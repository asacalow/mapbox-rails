# MapBox.js for rails asset pipeline

[MapBox.js](https://github.com/mapbox/mapbox.js) is a library integrating MapBox maps.

The `mapbox-rails` gem integrates the `Chosen` with the Rails asset pipeline.

## Usage

### Install mapbox-rails gem

Include `mapbox-rails` in Gemefile

    gem 'mapbox-rails'

Then run `bundle install`

### Include mapbox javascript assets

Add to your `app/assets/javascripts/application.js` 

    //= require mapbox.js

### Include mapbox stylesheet assets

Add to your `app/assets/stylesheets/application.css`

    *= require mapbox

and then conditionally require ```mapbox.ie``` as needed.

    <!--[if lte IE 8]>
      <%= stylesheet_link_tag    "mapbox.ie" %>
    <![endif]-->

### Enable mapbox 

    <div id='map' class='dark'></div>
    <script type='text/javascript'>
      var map = L.mapbox.map('map', 'examples.map-y7l23tes').setView([37.9, -77], 5);
    </script>

## Gem maintenance

Maintain `mapbox-rails` gem with `Rake` commands.

Update origin mapbox source files.

    rake update-mapbox

Publish gem.

    rake release

## License

Portions of this code use the BSD and the MIT license. See LICENSE.md for more information.