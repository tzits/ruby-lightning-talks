# GEOCODER

The power of api requests made easy with HTTP Party!

## Whats So Great About GEOCODER

<li> Easily converts from address to long and lat
<li> It allows for easy integration with Googlemaps API
<li> Also comes with reverse_geocode functionality

## Why use Geocoder

Geocoder is a complete geocoding solution for Ruby. With Rails, it adds geocoding (by street or IP address), reverse geocoding (finding street address based on given coordinates), and distance queries. It's as simple as calling geocode on your objects, and then using a scope like Venue.near("Billings, MT").
## Demo the awesomeness of this gem!

## Examples

Need to send authorization tokes and ids?!

```Ruby
class Person < ApplicationRecord
  geocoded_by :full_street_address
  after_validation :geocode

  def full_street_address
    [address,city,state,zipcode].join(', ')
  end
end
```

**Or**

```Ruby
  create_table "people", force: :cascade do |t|
    t.string   "first_name"
    t.string   "last_name"
    t.string   "address"
    t.string   "city"
    t.string   "state"
    t.string   "zipcode"
    t.datetime "created_at", null: false
    t.datetime "updated_at", null: false
    t.float    "latitude"
    t.float    "longitude"
  end
```

**Or if you want to get fancy**

```Ruby
<div> <%= image_tag "http://maps.googleapis.com/maps/api/staticmap?center=#{@person.latitude},#{@person.longitude}
&markers=#{@person.latitude},#{@person.longitude}&zoom=12&size=640x400&key=AIzaSyA4BHW3txEdqfxzdTlPwaHsYRSZbfeIcd8",
              class: 'img-fluid img-rounded', alt: "#{@person.first_name} on the map"%></div>

```

## Setup?

Just do: *gem install geocoder*

If you want to use in a rails app be sure to add the gem to your gemfile.

## Resources

<li> [Github and Docs](https://github.com/alexreisner/geocoder)
<li> [Site devoted to setup and advance function](http://www.rubygeocoder.com/)
