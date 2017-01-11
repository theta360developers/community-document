
![doc banner](http://theta360.guide/community-document/img/livestreaming/doc-banner.png)

Enable Live Streaming Mode
==========================

With the THETA off, press and hold the *mode* button. Keep pressing mode
and then press *power*. The camera will go into live streaming mode.

![Start THETA in LiveStreaming mode](http://theta360.guide/community-document/img/livestreaming/mode-buttons.png)

With the camera in live streaming mode, the word *Live* will appear in
blue.

![Verify that the camera’s *Live* light is on](http://theta360.guide/community-document/img/livestreaming/live-light.png)

Connect Camera to Computer
==========================

Plug the camera into your computer with a micro USB cable. It will
appear as a normal webcam. The camera will be called *RICOH THETA S*.

![Confirm you can see *RICOH THETA S* as a webcam](http://theta360.guide/community-document/img/livestreaming/skype-webcam.png)

The THETA is now streaming in dual-fisheye mode. The stream is 1280x720
at 15fps. The data is in MotionJPEG format.

Install Live Streaming Software
===============================

To stream the video to YouTube, install the official [RICOH
Live-streaming app](https://theta360.com/en/support/download/) and
[OBS](https://obsproject.com/).

> **Note**
>
> Many software can be used to stream to YouTube. Refer to [YouTube Live
> Verified Devices and
> Software](https://support.google.com/youtube/answer/2907883?hl=en) for
> more information.

Download and Install RICOH Live-Streaming App
---------------------------------------------

[Download](https://theta360.com/en/support/download/)

![Download the RICOH Live-Streaming App](http://theta360.guide/community-document/img/livestreaming/live-streaming-download.png)

1.  Select Windows 32bit, Windows 64bit, or Mac

2.  Turn your THETA off

3.  Unplug THETA from your computer

4.  Install software

![Live-Streaming App File is Called UVC Blender](http://theta360.guide/community-document/img/livestreaming/uvcblender-install.png)

With the THETA turned off, the software will prompt you to reconnect the
THETA to register your camera.

![Register THETA with computer](http://theta360.guide/community-document/img/livestreaming/register.png)

After you connect your THETA, a *Register* button will appear.

![Register buttons appears after connection](http://theta360.guide/community-document/img/livestreaming/register-button.png)

Complete the registration.

![Camera and computer registration complete](http://theta360.guide/community-document/img/livestreaming/registration-complete.png)

Test the THETA UVC Blender driver with any software that works with a
webcam. In the example below, I am using Skype.

![Testing THETA UVC Blender with Skype](http://theta360.guide/community-document/img/livestreaming/theta-uvc-skype-select.png)

> **Caution**
>
> Make sure you select *THETA UVC Blender* and not *RICOH THETA S*.

> **Note**
>
> In Skype, the video does not have 360° navigation (as of Oct 2016) and
> it will look like a distorted rectangle. Skype is for testing only,
> not for use.

Download and Install OBS
------------------------

![OBS Studio](http://theta360.guide/community-document/img/livestreaming/obs-icon.png)

[Download OBS](https://obsproject.com/)

Create a new *Scene*. Any name is fine. Click on the plus sign. Under
*Sources*, add THETA UVC Blender (any name is fine) and add a video
capture device. Right click to open the pop-up menu.

![Add Video Capture Device to OBS *Sources*](http://theta360.guide/community-document/img/livestreaming/obs-video-capture.png)

Select *THETA UVC Blender* as the Device. Verify that the video stream
is in equirectangular format.

![Verify THETA UVC Blender works in OBS](http://theta360.guide/community-document/img/livestreaming/obs-device.png)

> **Tip**
>
> If you see a black screen that says *Status:0x800705AA*, try to toggle
> your device between your two webcams. If you still see the error,
> disconnect all other webcams or disable the webcam on your laptop and
> then reboot your computer. The error above indicates that a connection
> is not established. See Troubleshooting section below

Leave the Resolution/FPS Type as *Device Default*.

![Leave Resolution/FPS Type as Default](http://theta360.guide/community-document/img/livestreaming/resolution-fps.png)

Under Settings → Video, set the resolution to 1280x720.

![Configure Resolution to 1280x720](http://theta360.guide/community-document/img/livestreaming/obs-settings-video.png)

> **Note**
>
> As of Oct 2016, the maximum resolution for UVC Blender is 720p. It’s
> likely that a higher resolution driver may be available in the future.
> Please check the maximum resolution and adjust your settings if
> needed.

Select Stretch to screen.

![obs stretch to screen](http://theta360.guide/community-document/img/livestreaming/obs-stretch-to-screen.png)

Create a YouTube Live 360° Event
================================

Log into YouTube. Click on the *Upload* button. Click the *Get started*
button on live streaming.

![Click Live Streaming after you click upload](http://theta360.guide/community-document/img/livestreaming/youtube-livestream.png)

Select *Events*.

![Select Events](http://theta360.guide/community-document/img/livestreaming/youtube-event.png)

> **Warning**
>
> Make sure you select Events. You will not get a 360° stream with
> *Stream now*.

In the right side of the screen, select *New live event*.

![New live event](http://theta360.guide/community-document/img/livestreaming/youtube-new-live-event.png)

Add a title.

Select Advanced Settings

![youtube advanced settings](http://theta360.guide/community-document/img/livestreaming/youtube-advanced-settings.png)

Select *This live stream is 360*.

![Select *This live stream is 360*](http://theta360.guide/community-document/img/livestreaming/youtube-livestream360.png)

Grab stream name from *Ingestion Settings*

![youtube ingestion 1](http://theta360.guide/community-document/img/livestreaming/youtube-ingestion-1.png)

Once you click on *Basic ingestion* information on your encoder will
open up.

![youtube basic ingestion](http://theta360.guide/community-document/img/livestreaming/youtube-basic-ingestion.png)

Copy the stream name. You will need this for OBS. In OBS, it is called,
*Stream key*.

![youtube streamname](http://theta360.guide/community-document/img/livestreaming/youtube-streamname.png)

Open OBS, go to Settings → Stream. Paste the YouTube stream name into
the box on OBS called, *Stream key*.

![obs streamkey](http://theta360.guide/community-document/img/livestreaming/obs-streamkey.png)

On the main OBS front control panel, press *Start Streaming* in the
right hand side of the control panel.

![obs start streaming](http://theta360.guide/community-document/img/livestreaming/obs-start-streaming.png)

On YouTube, go to the *Live Control Room* and click *Preview Stream*.

![youtube preview](http://theta360.guide/community-document/img/livestreaming/youtube-preview.png)

You can preview the stream if you have good bandwidth. I have limited
upstream bandwidth in my office. I reduced the ingestion bandwidth,
making my resolution lower.

![youtube preview test](http://theta360.guide/community-document/img/livestreaming/youtube-preview-test.png)

When you’re ready, start the stream.

![youtube streaming](http://theta360.guide/community-document/img/livestreaming/youtube-streaming.png)

Using HDMI
==========

Using USB output for live streaming, you will get a maximum resolution
of 720p. If you save your video files to your camera, the resolution
will be 1920x1080. If you save still images as timelapse, you can get
5376x2688, which will be displayed as 4K on YouTube.

The THETA S has an HDMI port that can output 1920x1080 at 30fps. In
order to use this signal, you need to use something like
[Blackmagicdesign UltraStudio for
Thunderbolt](https://www.blackmagicdesign.com/products/ultrastudiothunderbolt).

Once you get the video stream onto your computer, it will be in
dual-fisheye. To get this into equirectangular, you will need to use a
third-party product such as [Streambox Cloud
Encoder](http://theta360.guide/showcase/ricoh-product-streambox.html) or
MimoLive.

Streambox
---------

![streambox theta](http://theta360.guide/community-document/img/livestreaming/streambox-theta.png)

This is the workflow.

![streambox workflow](http://theta360.guide/community-document/img/livestreaming/streambox-workflow.png)

This is a [sample of the live stream using a
THETA](https://www.youtube.com/watch?v=d8TN_Vc6wL0).

![streambox sample](http://theta360.guide/community-document/img/livestreaming/streambox-sample.png)

This is the equipment and service list used:

-   Streamed live using Streambox Cloud Encoder

-   RICOH THETA S Camera

-   BlackMagic UltraStudio Mini Recorder

-   MacBook Pro with USB Modems

-   Streambox Cloud

mimoLive
--------

Boinx Software offers [mimoLive](https://boinx.com/mimolive/).

They have a good video that provides an [overview of their
service](https://youtu.be/nNQES53S2jc) specifically for the THETA S.

mimoLive can accept a USB or HDMI stream in dual-fisheye.

In order to use the HDMI output from the THETA, you will need a HDMI
video grabber. Boinx Software recommends the Blackmagic Design
[UltraStudio](https://www.blackmagicdesign.com/products/ultrastudiothunderbolt)
Mini Recorder for Thunderbolt or the [Magewell USB Capture HDMI adapter
for USB 3](http://www.magewell.com/usb-capture-hdmi).

![Getting THETA S HDMI Output Into Your Computer](http://theta360.guide/community-document/img/livestreaming/mimolive/hdmi-usb.png)

![mimoLive dual-fisheye before conversion to equirectangular](http://theta360.guide/community-document/img/livestreaming/mimolive/dual-fisheye.png)

mimoLive can take the THETA S dual-fisheye video stream source and apply
a filter convert it to equirectangular for streaming to places like
YouTube Live 360 events.

![Preset configuration and filter for THETA S](http://theta360.guide/community-document/img/livestreaming/mimolive/sources-thetas.png)

![Filter converts dual-fisheye stream to equirectangular](http://theta360.guide/community-document/img/livestreaming/mimolive/placerlive.png)

mimoLive provides sliders to adjust the sphere stitching. You’ll only be
able to get a *good enough* stitch. The edges of the spheres will not
match perfectly.

![Use sliders to adjust sphere edges](http://theta360.guide/community-document/img/livestreaming/mimolive/adjustment.png)

This is an example of the [360 live
stream](https://youtu.be/8CEB2_YQgkU). The quality of the stitch is
good.

Even if you are using USB output, you still may want to use mimoLive
instead of the free RICOH THETA UVC Blender app to take advantage of
mimoLive features to add text, Twitter, and slides into the YouTube live
streaming event.

![Place text into live stream to YouTube](http://theta360.guide/community-document/img/livestreaming/mimolive/text-placement360.png)

![Insert Twitter into live stream to YouTube](http://theta360.guide/community-document/img/livestreaming/mimolive/twitter.png)

![Insert presentation slides into 360 live stream](http://theta360.guide/community-document/img/livestreaming/mimolive/slides.png)

You can also center your video stream.

![Center 360 live stream](http://theta360.guide/community-document/img/livestreaming/mimolive/adjust-center.png)

[Example Stream Archive](https://youtu.be/8CEB2_YQgkU)

Other
-----

[Videostream360](http://shop.videostream360.com/vr-cams-equipment/360camera)
offers a service to use THETA at 1920x1080 with HDMI. They even sell the
THETA on their site.

If you have a solution for HDMI 360° streaming and you’ve verified that
it works with the THETA, please join the [THETA
Ecosystem](http://theta360.guide/ecosystem/) and
[post](http://lists.theta360.guide/c/theta-media/ecosystem-discussion)
information about it.

Tethered Streaming with Unity
=============================

Please refer to this [separate
article](http://lists.theta360.guide/t/using-ricoh-theta-live-view-with-unity/70?u=codetricity)
on using Unity with a tethered THETA.

Untethered WiFi Streaming
=========================

Streaming from the THETA using WiFi is primarily of interest to
developers and hobbyists.

Using Unity
-----------

The THETA can live stream a 640x320 MotionJPEG at 10fps over WiFi. This
is intended to preview a picture prior to taking the picture. It’s not
intended for headset navigation. The community has built some solutions
to stream this low-res, low fps video to mobile phones, primarily using
Unity.

This is a short Vine video of a [demo](https://vine.co/v/eV9XDQBEujt).

![360° video stream using WiFi](http://theta360.guide/community-document/img/livestreaming/wifi-unity.png)

Most developers have challenges processing the MotionJPEG stream.

Fortunately, [sample
code](https://github.com/theta360developers/ThetaWifiStreaming) of a
THETA S WiFi streaming demo with Unity was developed by community member
[Makoto Ito](https://github.com/makoto-unity). I’ve translated the
[README](https://github.com/makoto-unity/ThetaWifiStreaming/blob/master/README.md)
to his code as well as a [related
blog](http://noshipu.hateblo.jp/entry/2016/04/21/183439) written by
[@noshipu](https://twitter.com/noshipu), CEO of [ViRD,
Inc](http://vird.co.jp/) for his contribution.

### About the RICOH THETA API

In order to use Wifi live streaming, you must use the `_getLivePreview`
API. [Official
Reference](https://developers.theta360.com/en/docs/v2.0/api_reference/commands/camera._get_live_preview.html)

> NOTE from Craig: This was replaced by
> [getLivePreview](https://developers.theta360.com/en/docs/v2.1/api_reference/commands/camera.get_live_preview.html)
> in version 2.1 of the API. This blog by Noshipu-san refers to the 2.0
> API, which is still supported by the THETA S. Be aware of the
> differences in your code.

Unlike the other APIs, `_getLivePreview` is different because the data
is in a stream and keeps going. You will not be able to get a WWW class
to wait until the request is complete (maybe).

> NOTE from Craig: This is the major problem developers have when
> working with `getLivePreview`. As the data is a stream, you can’t want
> for the data to end before running your next command. For example,
> it’s different from downloading and displaying an image or video file
> because you know when the transfer is complete.

### Processing Flow
#### Set the POST request to create a HttpWebRequest class

    string url = "Enter HTTP path of THETA here";
    var request = HttpWebRequest.Create (url);
    HttpWebResponse response = null;
    request.Method = "POST";
    request.Timeout = (int) (30 * 10000f); // to ensure  no timeout
    request.ContentType = "application/json; charset = utf-8";

    byte [] postBytes = Encoding.Default.GetBytes ( "Put the JSON data here");
    request.ContentLength = postBytes.Length;

#### Generate a class of BinaryReader to get the byte data (you get the bytes one by one)

    // The start of transmission of the post data
    Stream reqStream = request.GetRequestStream ();
    reqStream.Write (postBytes, 0, postBytes.Length) ;
    reqStream.Close ();
    stream = request.GetResponse () .GetResponseStream ();

    BinaryReader reader = new BinaryReader (new BufferedStream (stream), new System.Text.ASCIIEncoding ());

#### Get the start and stop bytes of 1 frame of the MotionJPEG and cut out one frame

With the byte, check the partion value of the MotionJPEG.

    ...(http)
    0xFF 0xD8      --|
    [jpeg data]      |--1 frame of MotionJPEG
    0xFF 0xD9      --|
    ...(http)
    0xFF 0xD8      --|
    [jpeg data]      |--1 frame of MotionJPEG
    0xFF 0xD9      --|
    ...(http)

Please refer this answer on StackOverflow to [How to Parse MJPEG HTTP
stream from IP
camera?](http://stackoverflow.com/questions/21702477/how-to-parse-mjpeg-http-stream-from-ip-camera)

The starting 2 bytes are `0xFF, 0xD8`. The end bye is `0xD9`

The code is shown below.

    List<byte> imageBytes = new List<byte> ();
    bool isLoadStart = false; // Binary flag taken at head of image
    byte oldByte = 0; // Stores one previous byte of data
    while( true ) {
        byte byteData = reader.ReadByte ();

    if (!isLoadStart) {
        if (oldByte == 0xFF){
            // First binary image
           imageBytes.Add(0xFF);
        }
        if (byteData == 0xD8){
           // Second binary image
           imageBytes.Add(0xD8);

           // I took the head of the image up to the end binary
           isLoadStart = true;
        }
    } else {
        // Put the image binaries into an array
        imageBytes.Add(byteData);

            // if the byte was the end byte
            // 0xFF -> 0xD9 case、end byte
            if(oldByte == 0xFF && byteData == 0xD9){
                // As this is the end byte
                // we'll generate the image from the data and can create the texture
                // imageBytes are used to reflect the texture
                // imageBytes are left empty
                // the loop returns the binary image head
                isLoadStart = false;
            }
        }
        oldByte = byteData;
    }

#### Texture Generation Separated by Byte

This is the byte to reflect the texture.

    mainTexture.LoadImage ((byte[])imageBytes.ToArray ());

Portion of Python code taken from [StackOverflow
answer](http://stackoverflow.com/questions/21702477/how-to-parse-mjpeg-http-stream-from-ip-camera).

    import cv2
    import urllib
    import numpy as np

        stream=urllib.urlopen('http://localhost:8080/frame.mjpg')
        bytes=''
        while True:
            bytes+=stream.read(1024)
            a = bytes.find('\xff\xd8')
            b = bytes.find('\xff\xd9')
            if a!=-1 and b!=-1:
                jpg = bytes[a:b+2]
                bytes= bytes[b+2:]
                i = cv2.imdecode(np.fromstring(jpg, dtype=np.uint8),cv2.CV_LOAD_IMAGE_COLOR)
                cv2.imshow('i',i)
                if cv2.waitKey(1) ==27:
                    exit(0)
    Mjpeg over http is multipart/x-mixed-replace with boundary frame info and jpeg data is just sent in binary. So you don't really need to care about http protocol headers. All jpeg frames start with marker 0xff 0xd8 and end with 0xff 0xd9. So the code above extracts such frames from the http stream and decodes them one by one. like below.

    ...(http)
    0xff 0xd8      --|
    [jpeg data]      |--this part is extracted and decoded
    0xff 0xd9      --|
    ...(http)
    0xff 0xd8      --|
    [jpeg data]      |--this part is extracted and decoded
    0xff 0xd9      --|
    ...(http)

#### Testing WiFi Streaming

You can test out WiFi Streaming without having to program. Download and
install [Unity Personal
Edition](https://store.unity.com/products/unity-personal). It’s free.

Get Makoto Ito’s code for
[ThetaWifiStreaming](https://github.com/theta360developers/ThetaWifiStreaming).

Press *Play*.

![Unity WiFi Live Stream in Game Mode](http://theta360.guide/community-document/img/livestreaming/unity/wifi/game-view-crop.png)

![Unity Scene View of WiFi Live Stream](http://theta360.guide/community-document/img/livestreaming/unity/wifi/scene-4-crop.png)

![Top down view of sphere with THETA camera positions](http://theta360.guide/community-document/img/livestreaming/unity/wifi/top-down-sphere.png)

Using a Raspberry Pi
--------------------

A Raspberry Pi can take the video live stream from the THETA using USB
and transmit the stream to another device using WiFi. This is intended
for software developers to use as starting point.

There is [sample
code](https://github.com/theta360developers/video-streaming-sample-app)
available for both the transmission of the live stream and the
conversion of the live stream into a navigable 360 video. Both the
browser and the server applications are written in JavaScript. The
server application uses node.

![video stream prior to conversion](http://theta360.guide/community-document/img/livestreaming/thetaview-fisheye.png)

The sample code uses JavaScript to convert the dual-fisheye video stream
into a navigable 360° video. Transmission uses
[WebRTC](https://webrtc.org/).

![stream conversion done in browser](http://theta360.guide/community-document/img/livestreaming/thetaview-360view.png)

FAQ
===

**Q: What’s the Resolution and FPS?**

**A:** Updated Oct 2016.

**Q: Can I stream from a drone to a headset?**

**A:** Only with expensive equipment. This is not a good use of the
THETA for recreational hobbyists. [Refer to this
article](http://lists.theta360.guide/t/using-theta-360-video-from-a-drone/133?u=codetricity)
for more information.

**Q: Does the THETA have auto-stabilization?**

**A:** No. You’ll need to use a third-party
[gimbal](http://lists.theta360.guide/t/theta-s-dokumentation-on-a-clasic-mc-rally/211/11?u=codetricity).

**Q: Is anyone using the THETA 360° stream for object recognition?**

**A:** Yes. Most people use the raw video from 2 fisheye spheres. Most
people do not convert to equirectangular video. Just extract a portion
of the sphere and perform the image recognition or measurement on that
section. The HDMI stream has higher resolution. Most people are using
that and extracting a frame, then performing the calculation. Known
applications include facial recognition, audience emotion recognition,
autonomous vehicle operation. As just one example, the winner of the
RICOH prize at the 2016 DeveloperWeek Hackathon used the [Microsoft
Emotion
API](https://www.microsoft.com/cognitive-services/en-us/emotion-api) on
the dual-fisheye spheres.

**Q: Is anyone working on panoramic sound?**

**A:** Yes. There are many projects for 3D sound, including
[SOPA](http://lists.theta360.guide/t/panoramic-videos-with-panoramic-sounds/304?u=codetricity),
an open source JavaScript library.

**Q: How do I increase the sound quality?**

**A:** Use an external microphone and add it to your mixer. Set the
THETA’s input to zero using your mixer. If you’re using OBS for the
stream, plug your microphones into your computer and then add a new
audio source from the main dashboard to your stream. There is no way to
plug a microphone directly into the THETA.

![OBS mixer](http://theta360.guide/community-document/img/livestreaming/mixer.png)

Troubleshooting
===============

Streaming to YouTube
--------------------

### Problem: Status:0x800705AA

![Error message when device not detected](http://theta360.guide/community-document/img/livestreaming/obs-error.png)

1.  Verify your firmware is 01.42 or above

2.  Make sure your camera has the blue word `Live` in LED lights on

3.  Toggle between webcam and UV Blender. If this still fails to resolve
    the problem, disable all other webcams and reboot

4.  Try a different USB cable. Plug it into the port on the back of your
    computer

### Problem: Screen is black with nothing on it

Check video resolution. Set to 1280x720

### Problem: Video on YouTube is Equirectangular with No Navigation

If the stream is in equirectangular on OBS and it can’t be navigated on
YouTube, check your YouTube configuration.

Heat
----

The unit below overheated 16 minutes into the shoot. It is using UVC
Blender and a USB cable during an indoor shoot at Stanford during a
crowded VR event.

![Overheating during livestream](http://theta360.guide/community-document/img/livestreaming/heat/overheat-example.png)

If the THETA is overheating, point a standard household fan at it. The
airflow may be enough to cool the outside of the THETA and help with the
internal overheating.

People have reported success by sticking \$6 Raspberry Pi heatsinks onto
the body of the THETA or taping or attaching a small fan used for
computer CPUs to the outside of the THETA.

![Raspberry Pi Heatsinks (L), small computer fan bracket ®](http://theta360.guide/community-document/img/livestreaming/heat/heatsinks.png)

-   [6 piece Addicore heatsink](https://amzn.com/B00LKX618Q) for
    Raspberry Pi for \$5.95

-   [Mudder 8 piece black heatsink cooler for
    RPi](https://amzn.com/B01GE7Q060) for \$6.99

-   [TinkerCad Fan Holder for 3D
    printing](https://www.tinkercad.com/things/7oICypvba1i-theta-s-cooling-fan-holder)

The enthusiast below created custom cases in plastic through a shop in
Akihabara. He wanted to use metal, but the cost was too high.

![Not recommended, but an example of community enthusiasm](http://theta360.guide/community-document/img/livestreaming/heat/case-mod.png)
