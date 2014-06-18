<h2>Geofencing Explained</h2>

## What's All This About?

TODO(slightlyoff): explain motivation for feature here.

## Registering A Geofence

Registering for a geofence is straightforward:

```html
<!DOCTYPE html>
<!-- https://app.example.com/index.html -->
<html>
  <head>
    <script>
      navigator.serviceWorker.register("/sw.js");

      navigator.serviceWorker.whenReady().then(function(sw) {
        // TODO
      });
    </script>
  </head>
  <body> ... </body>
</html>
```

## Handling Geofence Events

Location notification happens from the Service Worker context via the new `...` event.

```js
// sw.js
self.<...> = function(event) {
  // TODO
};
```

## Removing Geofences
```js
// TODO
```

## Notes

  * Since Service Workers are a requirement for Geofencing, and since Service Workers are limited to HTTPS origins, sites served without encryption will always fail to register for fences.
  * SW event handlers aren't allowed to run forever.
