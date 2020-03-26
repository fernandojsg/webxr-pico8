# webxr-pico8
WebXR Pico8 Player: https://fernandojsg.github.io/webxr-pico8/

![screenshot](https://fernandojsg.github.io/webxr-pico8/assets/screenshot.png)

# Introduction
Proof of concept on how to integrate already existing non immersive games in a WebXR application.
I used [pico-8](https://www.lexaloffle.com/pico-8.php) games in this example as you can export them to self-contained html&js without external dependencies, but this concept could be applied to any game as you just need to get the `canvas` where the game is being rendered.

I loaded the `pico-8` carts using an `iframe` and I resend all the keyboard events the main document gets to that `iframe`.

The `WebXR` version is currently developed to work just with `Oculus Quest` at the moment, but I'll extend the support of other devices later on.
I used the IW WG [WebXR input profiles library](https://github.com/immersive-web/webxr-input-profiles) to detect the buttons and axis state and convert it to key events and send them to the pico8 `iframe`.

It's important to notice that when entering VR, the `window.requestAnimationFrame` is not being called, so you should handle it correctly in your game in order to get it rendered and executed properly.

# Credits
Assets:
* [Hall model](https://github.com/MozillaReality/hello-webxr/blob/master/assets/hall_variants/hall_empty.glb) ([Hello WebXR variant](https://github.com/mozillareality/hello-webxr)) by [Diego Goberna](https://twitter.com/feiss)

Pico-8 Carts:
* [Celeste by noel](https://www.lexaloffle.com/bbs/?tid=2145)
* [The Merciless Deep  by oule](https://www.lexaloffle.com/bbs/?tid=36914)
* [Desert drift  by np](https://www.lexaloffle.com/bbs/?pid=55232)
* [Katamari  by p01](https://www.lexaloffle.com/bbs/?uid=28958)
* [Polar panic  by anp](https://www.lexaloffle.com/bbs/?tid=36118)
* [X-Wing Pico Squadron by xavier](https://www.lexaloffle.com/bbs/?tid=28996)
* [X-Zero  by  "paranoidcactus](https://www.lexaloffle.com/bbs/?tid=36053)
* [Tomb of G'Nir  by oidcactus](https://www.lexaloffle.com/bbs/?pid=52574)
* [Pico Tennis  by noidcactus](https://www.lexaloffle.com/bbs/?tid=31450)
