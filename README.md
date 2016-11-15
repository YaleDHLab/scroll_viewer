# Scroll Viewer
Support for zoomified large images + cursor positioning

Phto
You will need to adjust the height and width `index.html`:

```javascript
	var layer = L.tileLayer.zoomify('imagetiles/{g}/{z}-{x}-{y}.jpg', {
			width: Type the width in pixels here,
			height: Type the height in pixels here,
			attribution: ''
		}).addTo(map);
```    
