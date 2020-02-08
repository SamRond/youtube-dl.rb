Ruby wrapper for [youtube-dl](http://rg3.github.io/youtube-dl/).

### Install the gem

**IMPORTANT NOTE:** The [`youtube_dl`](https://github.com/ystomar-work/youtube_dl) gem and the [`ruby-youtube-dl`](https://github.com/bnmrrs/ruby-youtube-dl) gem will [cause a conflict](https://github.com/layer8x/youtube-dl.rb/issues/24) with this gem. Please `gem uninstall` those gems before using this one.

Add this line to your application's Gemfile:

```ruby
gem 'youtube-dl.rb'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install youtube-dl.rb

### Usage

Pretty simple.

```ruby
YoutubeDL.download "https://www.youtube.com/watch?v=gvdf5n-zI14", output: 'some_file.mp4'
```

All options available to youtube-dl can be passed to the options hash

```ruby
options = {
  username: 'someone',
  password: 'password1',
  rate_limit: '50K',
  format: :worst,
  continue: false
}

YoutubeDL.download "https://www.youtube.com/watch?v=gvdf5n-zI14", options
```

Options passed as `options = {option: true}` or `options = {option: false}` are passed to youtube-dl as `--option` or `--no-option`

### Updating Binaries
To update the youtube-dl binaries, follow these steps:
1. Run `rake binaries:update`
2. Commit & push

It's that easy!