# Note: This repository has been archived
This project was developed under a previous phase of the Yale Digital Humanities Lab. Now a part of Yale Library’s Computational Methods and Data department, the Lab no longer includes this project in its scope of work. As such, it will receive no further updates.

# Scroll Viewer
Support for zoomified large images + cursor positioning

Photoshop: File > Export > Zoomify

Specify which folder to export into (ideally an empty folder iwth the name of the scroll.)

Use `imagetiles` as the "Basename". 

Once the export is complete, delete `imagetiles.html` and `ZoomifyImageViewer-min.js`, leaving only the `imagetiles` directory. Download and unzip all the files in this repository and put them in the folder with the `imagetiles` folder. The final diectory listing should be:

```
├── Control.FullScreen.css
├── Control.FullScreen.js
├── L.Control.MousePosition.css
├── L.Control.MousePosition.js
├── L.TileLayer.Zoomify.js
├── README.md
├── icon-fullscreen-2x.png
├── icon-fullscreen.png
├── imagetiles
│   ├── ImageProperties.xml
│   └── TileGroup0
│       ├── 0-0-0.jpg
│       ├── (hundreds of more files here...)
├── index.html
├── jquery.smoothZoom.min.js
├── leaflet.css
├── leaflet.js
├── leaflet.zoomdisplay.css
├── leaflet.zoomdisplay.js
└── styles.css
```

You will need to adjust the height and width in the `index.html` file.  Replace `WIDTH_IN_PIXELS` and `HEIGHT_IN_PIXELS` with their correct values:

```javascript
	var layer = L.tileLayer.zoomify('imagetiles/{g}/{z}-{x}-{y}.jpg', {
			width: WIDTH_IN_PIXELS,
			height: HEIGHT_IN_PIXELS,
			attribution: ''
		}).addTo(map);
```    
You will need to adjust the number of folders (`TileGroup0`, `TileGroup1`, etc) in the `index.html` file:

		var numTileFolders = 1;
