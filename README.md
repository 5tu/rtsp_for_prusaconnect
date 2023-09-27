# RTSP for PrusaConnect
Run this script to regularly capture a snapshot and upload to PrusaConnect. If your RTSP camera is unavilable then the script will periodically check for it's availabilty before resuming.

### Prerequisites
- FFmpeg

### Instructions
- Create a new PrusaConnect camera by selecting 'Add new web camera'.
- Click on the pairing QR code, or open a new browser window/tab and append the generated token to:
```
https://webcam.connect.prusa3d.com/?token=
```
- Use your browser's inspector tool to view the page's network activity (you may need to refresh the page).
- Under 'info' you can find the fingerprint value.
- Place the script in a folder on your computer you wish to run it from.
– Using a text editor, edit the script to change the following variables;
  - `camera_ip` – the IP address of the RTSP camera you're using.
  - `camera_rtsp_url` – the RTSP URL for the camera stream.
  - `token` – the token generated by PrusaConnect.
  - `fingerprint` – the fingerprint value you found using the inspector tool.

- Make sure it is executable:
```
chmod +x rtsp_for_prusaconnect.sh
```
- Then run the script:
```
./rtsp_for_prusaconnect.sh
```
- To exit, press Ctrl+C – or close the terminal window.

### More info
If your camera supports a higher resolution, the image will be resized to a horizontal resolution of 1920px.
