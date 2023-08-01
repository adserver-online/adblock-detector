# Adblock Detection Script. Free, Simple, and Efficient.

The script is based on the bait CSS method, but it also has an "extended" mode in which the script can request an external URL to check whether it is blocked.

Extended mode is disabled by default so the script does not perform any HTTP requests.

## Installation

1. Download ```ab-detect.js``` file and host it on your webserver 
2. Add script loading to HEAD or BODY section of your website: ```<script src="ab-detect.js" async></script>```
3. Call the detector by placing following code in BODY section of your webpages:

```
window.addEventListener('load', function () {
    DetectAb(function (result) {
        if (result) {
            // ad block detected
        }
    });
});
```

## Extended mode

This mode is more reliable, but it performs extra HTTP request.

To enable extended mode, you need to pass ```true``` as second parameter of ```DetectAb``` function:

```
DetectAb(function (result) {
  // handle result
}, true);
```

## Demo

Check out ```demo.html``` for working example.

