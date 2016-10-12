# HTTP Party

The power of api requests made easy with HTTP Party!

## Whats So Great About HTTP Party

<li> Setting all the headers!
<li> Making life easy with apis!
<li> JSON on JSON on JSON!

## Demo the awesomeness of this gem!

<li> httparty "https://api.stackexchange.com/2.2/questions?site=stackoverflow"
<li> httparty "http://food2fork.com/api/search?key=ac89596132bf565718f0859218dadf7f&q=shredded%20cheese"

## Examples

Need to send authorization tokes and ids?!

```Ruby
auth = {
  user_id: "dt_SAMPLETOKENd88ffc342dde5c195df4019f90d6ed",
  token: "super_s3cr3t_h@$hed_t0k3n_h3Re"
}
options = { basic_auth: auth }

result = HTTParty.get("https://api.stackexchange.com/2.2/questions?site=stackoverflow", options)
```

**Or**

```Ruby
  key = "ac89596132bf565718f0859218dadf7f"

  HTTParty.get("http://food2fork.com/api/search?key=" + key + "&q=shredded%20cheese")
```

**Finally the official setup in RoR**

```Ruby
require 'httparty'

class Twitter
  include HTTParty
  base_uri 'twitter.com'
  basic_auth 'username', 'password'
end

puts Twitter.post('/statuses/update.json', :query => {:status => "It's an HTTParty and everyone is invited!"}).inspect
```

## Setup?

Just do: *gem install httparty*

If you want to use in a rails app be sure to add the gem to your gemfile. 

## Resources

<li> [Github and Docs](https://github.com/jnunemaker/httparty)
<li> [Treehouse Blog About Setup](http://blog.teamtreehouse.com/its-time-to-httparty)
