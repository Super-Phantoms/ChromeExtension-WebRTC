# Chrome extension for WebRTC Screen Sharing

<a target="_blank" href="https://chrome.google.com/webstore/detail/webrtc-desktop-sharing/nkemblooioekjnpfekmjhpgkackcajhg"><img alt="WebRTC Screen Sharing" src="https://lh3.googleusercontent.com/hoWYXBvzcszyre-LlNVq5i_lEFtqVXYrTJ8gnkVw35vv5xWyUx7sw8VPMrGXjHpxUcV0n3Ie=w640-h400-e365" title="WebRTC Screen Sharing"></img></a>

<a target="_blank" href="https://chrome.google.com/webstore/detail/webrtc-desktop-sharing/nkemblooioekjnpfekmjhpgkackcajhg"><img alt="WebRTC Screen Sharing" src="https://lh3.googleusercontent.com/rUvbMYBGFgwbe_gzIj3qUwtlnemsvbHccSskM__tjFSIILN3D7QRS6P1LielPb90Wt2a4awmNg=w640-h400-e365" title="WebRTC Screen Sharing"></img></a>

## How to install?

<a target="_blank" href="https://chrome.google.com/webstore/detail/webrtc-desktop-sharing/nkemblooioekjnpfekmjhpgkackcajhg"><img alt="Install Dessktop Sharing Extension" src="https://raw.github.com/GoogleChrome/chrome-app-samples/master/tryitnowbutton_small.png" title="Click here to install this sample from the Chrome Web Store"></img></a>

* https://chrome.google.com/webstore/detail/webrtc-desktop-sharing/nkemblooioekjnpfekmjhpgkackcajhg

## How to view screen?

Try any of the below URL. Replace `your_room_id` with real room-id:

```
https://www.webrtc-experiment.com/screen/?s=your_room_id
```

## Developer Notes

1. Chrome extension can share your screen, tab, any application's window, camera, microphone and speakers.
2. Clicking extension icon will generate a unique random room URL. You can share that URL with multiple users and all of them can view your screen.
3. [RTCMultiConnection](https://github.com/Super-Phantoms/ChromeExtension-WebRTC) is a WebRTC library that is used for peer-to-peer WebRTC streaming.
4. PubNub is used as a signaling method for handshake. However you can use [any WebRTC signaing option](https://github.com/Super-Phantoms/ChromeExtension-WebRTC/blob/master/Signaling.md).
5. You can replace or include your own STUN+TURN servers in the [IceServersHandler.js](https://github.com/Super-Phantoms/ChromeExtension-WebRTC/blob/master/desktopCapture-p2p/IceServersHandler.js) file.
6. VP8 is currently default video codecs. However VP9 is recommended. You can always change codecs using options page.
7. [getStats](https://github.com/Super-Phantoms/ChromeExtension-WebRTC) is a WebRTC library that is used for bandwidth & codecs detection. This library is optional. You can always remove it.

## Before publishing it for your own business

> This step is optional. You can keep using `webrtc-experiment.com` URL as a screen viewer.

Open [desktop-capturing.js](https://github.com/Super-Phantoms/ChromeExtension-WebRTC/blob/master/desktopCapture-p2p/desktop-capturing.js) and find following line:

```javascript
var resultingURL = 'https://www.webrtc-experiment.com/screen/?s=' + connection.sessionid;
```

Replace above line with your own server/website:

```javascript
var resultingURL = 'https://yourWebSite.com/index.html?s=' + connection.sessionid;
```

You can find `index.html` here:

* [desktopCapture-p2p/index.html](https://github.com/Super-Phantoms/ChromeExtension-WebRTC/blob/master/desktopCapture-p2p/index.html)

## How to publish it for your own business?

Make ZIP of the directory. Then navigate to [Chrome WebStore Developer Dashboard](https://chrome.google.com/webstore/developer/dashboard) and click **Add New Item** blue button.

To learn more about how to publish a chrome extension in Google App Store:

* https://developer.chrome.com/webstore/publish

## For more information

For additional information, click [this link](https://github.com/Super-Phantoms/ChromeExtension-WebRTC/desktopCapture/README.md).

## It is Open-Sourced!

* https://github.com/Super-Phantoms/ChromeExtension-WebRTC/tree/master/desktopCapture-p2p

## License

[Chrome-Extensions](https://github.com/Super-Phantoms/ChromeExtension-WebRTC) are released under [MIT license](https://github.com/Super-Phantoms/ChromeExtension-WebRTCblob/master/LICENSE) . Copyright (c) [Super-Phantom].
