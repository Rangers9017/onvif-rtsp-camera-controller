# ONVIF + RTSP Camera Viewer

A small Python desktop prototype for viewing an RTSP camera stream and experimenting with ONVIF camera controls. The interface is built with PyQt5; video frames are read through OpenCV/FFmpeg.

**Languages:** Python · Turkish UI  
**License:** Apache-2.0

## Features

- Preview an RTSP stream in a desktop window.
- Connect to an ONVIF camera for media and imaging information.
- Prototype controls for brightness, IR-cut filter, and PTZ zoom.

The camera must support the relevant ONVIF services for those controls to work. This project is a prototype; camera models expose different capabilities.

## Requirements

- Python 3
- PyQt5
- OpenCV with an FFmpeg video backend
- `onvif-zeep`, `zeep`, and `requests`
- ONVIF WSDL files in the `./wsdl` directory expected by the current code

Install the Python packages:

```bash
python -m pip install PyQt5 opencv-python onvif-zeep zeep requests
```

## Run

```bash
python camera.py
```

Enter your own RTSP stream URL in the application. Configure ONVIF address and login details locally in `camera.py` when using the ONVIF features. **Do not commit camera URLs, passwords, or other credentials.** The project opens an ONVIF connection at startup, so a reachable camera and the WSDL directory are needed for that part.

## Notes

- Keep credentials on your own machine; the repository contains no default camera login.
- RTSP and ONVIF endpoints vary by camera manufacturer.
- The current app is an early prototype; not all visible controls are connected to settings actions yet.

## Türkçe

Bu depo, RTSP kamera görüntüsünü masaüstünde izlemek ve ONVIF kontrollerini denemek için hazırlanmış küçük bir Python prototipidir. Arayüz PyQt5, görüntü akışı OpenCV/FFmpeg ile çalışır.

- Kullanılan paketler: PyQt5, OpenCV, `onvif-zeep`, `zeep`, `requests`
- ONVIF için mevcut kodun beklediği `./wsdl` dizini gerekir.
- Kendi RTSP adresini uygulamaya yaz. ONVIF bilgilerini yalnızca yerel kopyanda ayarla; parolaları repoya ekleme.
- Kameranın desteklemediği ONVIF özellikleri çalışmayabilir.

Bu kod erken aşamadaki bir prototiptir; arayüzdeki tüm kontroller henüz ayarlara bağlanmış değildir.
