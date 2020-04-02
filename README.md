<p align="center">
<img src="img/bvplogo.png">
</p>

<p align="center">
<a href="./screenshots/d6.png"><img src="img/d6.png"></a>
<a href="./screenshots/d4.png"><img src="img/d4.png"></a>
<a href="./screenshots/d11.png"><img src="img/d11.png"></a>
<a href="./screenshots/d7.png"><img src="img/d7.png"></a>
<a href="./screenshots/d5.png"><img src="img/d5.png"></a>
</p>

<p align="center">
<a href="./screenshots/d8.png"><img src="img/d8.png"></a>
<a href="./screenshots/d10.png"><img src="img/d10.png"></a>
<a href="./screenshots/d12.png"><img src="img/d12.png"></a>
<a href="./screenshots/d17.png"><img src="img/d17.png"></a>
<a href="./screenshots/d18.png"><img src="img/d18.png"></a>
</p>

<p align="center">
<a href="./screenshots/d13.png"><img src="img/d13.png"></a>
<a href="./screenshots/d16.png"><img src="img/d16.png"></a>
<a href="./screenshots/d19.png"><img src="img/d19.png"></a>
<a href="./screenshots/d2.png"><img src="img/d2.png"></a>
<a href="./screenshots/d1.png"><img src="img/d1.png"></a>
</p>

# So what is this thing?

The **boundless video player** is an experimental web app that continuously
resamples a video's edge pixels during playback and projects them outwards in
3D, in effect removing that video's traditional boundaries. I originally created
this app to rekindle the nostalgia of classic 80's music videos, but in the
process of making it discovered it's fun to try on just about any type of video.

This app _should_ work on most devices, though be aware I primarily developed
this on desktop (Chrome browser) and tested on iPhone/iPad devices. For the best
viewing experience, a large display is recommended. FWIW it runs great on an
Ultra Widescreen monitor 😀

Click here to access the app: https://bvp.surge.sh/

# Known issues 🐜

-   iOS Chrome browser in landscape mode: Zoom toggles on unexpectedly causing
    misalignment ( please use Safari browser instead )

# Settings

![](img/settings.png)

To get the most out of this app, try playing around with the following settings
in realtime. ( Note: The URL is automatically updated to reflect your changes,
which can be shared out to others )

## **Select video**

A drop-down menu to choose between the available video samples.<br>_Each demo is
configured with custom presets, but you can override them after the video is
loaded._<br><br>📺You can also load your own custom videos by adding the
following URL parameter: `?v=<PATH_TO_YOUR_CUSTOM_VIDEO_URL>`<br>For best
results, use a non-DRM HTML5 video stream close in size to 640x360 or 480x360. You can
also optionally specify a starting timestamp with `#t=<SECONDS>`

## **Effects**

Additional effects you can apply to improve the visualization

-   **Show Vignette** - Whether to apply a shadowy radial gradient on the main
    view<br>![](img/fx-vig.png)<br>_( URL param: #vig=true )_

-   **Trippy Mode** - When activated, the expanded pixels are alpha-blended
    together, creating a neat smearing effect.<br>![](img/fx-trip.png)<br>_(URL
    param: #tr=true)_

-   **Vaporwave Mode** - Applies a cyan/magenta linear gradient to the
    view<br>Tip: To more authentically maximize the
    [Vaporwave](https://en.wikipedia.org/wiki/Vaporwave) experience, try also
    adjusting the playback rate to 0.7 or lower<br>![](img/fx-vw.png)<br>_(URL
    param: #vw=true)_

-   **Playback Rate** - Changes the video playback speed<br>_( URL param: #rate=R,
    where 0.1 <= R <= 2 )_

-   **Blurriness (pixels)** - Applies a Gaussian blur on the projection, based on
    the defined pixel radius<br>To disable the blur, set the value to 0.
    Recommended setting: 1<br>![](img/fx-blur2.png)<br>_( URL param: #blur=R, R =
    pixel radius )_

## **Projection**

Additional controls to fine-tune the expansion

-   **Expansion method** - The manner in which the boundary pixels of each video
    frame are expanded outwards

    -   _Fill screen_ - Pixels expand to fill the screen in a 3D perspective. (
        Default behavior ) <br>![](img/exp-fill.png)<br>_( URL param: #mode=0 )_

    -   _Spread evenly_: Pixels expand in a 3D perspective but equally in both
        directions<br>This pattern is mainly useful if you wish to improve the
        horizontal/vertical pixel alignment ( it may also help improve performance
        if you're on a slow device.)<br>![](img/exp-spread.png)<br>_( URL param:
        #mode=1 )_

    -   _2D_: Pixels expand only in the four cardinal
        directions.<br>![](img/exp-2d.png)<br>_( URL param: #mode=2 )_

    -   _None_: No expansion pattern is applied.<br>Choose this mode if you just
        want to see the main video<br>![](img/exp-none.png)<br>_( URL param:
        #mode=3 )_

-   **Show Video Edges** - Draws a white rectangle around the source region of the
    original video frame.<br>![](img/tune-border.png)<br>_( URL param:
    #border=true )_

-   **Video X/Y Offset (pixels)** - Sets the horizontal/vertical offsets of the
    cropped video from which the projection is based<br>Tip: Use this setting to
    eliminate projection gaps ( by moving offsets beyond pillarboxed regions and
    unwanted borders. )<br>![](img/tune-offsets.png)<br>_( URL param:
    #xOff=X&yOff=Y, X/Y = pixel offsets )_

-   **Input Size (pixels)**: Sets the # of edge pixels to sample from the source
    video frame<br>Tip: Set both input and output slices to a similar larger value
    if you want the projection to be more blocky.<br>![](img/tune-in.png)<br>_(
    URL param: #in=R, R = pixel radius )_

-   **Output Size (pixels)**: Sets the scaled pixel size of where the sampled edge
    pixels are redrawn.<br>Tip: Set this to a higher value if you want to increase
    the projection speed<br>![](img/tune-out.png)<br>_( URL param: #out=R, R =
    pixel radius )_

-   **About**: Opens up this document
-   **Share URL**: Generates a URL which reflects the video selection and settings and opens a Twitter dialog for sharing.

# Basic Controls

While the basic menu should give you direct access to playback and settings, the
following keyboard shortcuts are also available for more convenience

|            **Input**            | **Action**                                                                                |
| :-----------------------------: | ----------------------------------------------------------------------------------------- |
| Space<br>( or Click in window ) | Toggles both menu and video playback                                                      |
|              Enter              | Toggles settings                                                                          |
|             Escape              | Toggles video playback<br>( useful if you want to pause the screen to take a screenshot ) |

<br>Have fun!<br> [@joeycato](https://twitter.com/joeycato)
