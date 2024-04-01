# trip-page

### This is a trip page for Ember buses, written in vue3 with typescript.

- The home page proves a list of in-progress trips from the ember quotes api (https://ember-core.stoplight.io/docs/api-documentation/a79721f8123d9-get-quotes). This page is mainly to provide a convient way to access trips.
- The trip page can be accessed from the homepage, by selecting an item which routes to /trip/{tripId}

## Trip page features

- State fetched and updated periodically
  - Url and update frequency can be configured in [src\config.ts](src\config.ts)
- Interactive map with bus location and stops displayed
  - Stop marker color changes based on whether the stop is to be visited or not
  - Bus can be optionally "tracked"
  - Button to place marker and zoom to user location (if access to user location is enabled)
- List of stops with estimated and scehduled time displayed
  - "Estimated time" color will vary based on how late the bus might be
  - Click list items to zoom to them on the map
  - Bus "tracking" can be toggled (represented by the pin icon on the bus row)
  - Bus facilities (WiFi / WC) displayed

## ToDo

- Test coverage is thin and at best can be seen as an example / base to be built upon
- Styling is basic, intended for mobile screens but there are known issues (dark mode doesnt work well)
  - Styles are not inherited well
- Icons are mostly placeholder quality
- No real consideration yet for internationalization
- Some errors are logged to console or go to alert() but could be displayed better
