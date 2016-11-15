# Scroll Viewer
Support for zoomified large images + cursor positioning

Phto
You will need to adjust the height and width `index.html`:

```
	var layer = L.tileLayer.zoomify('imagetiles/{g}/{z}-{x}-{y}.jpg', {
			width: 3070,
			height: 24502,
			attribution: ''
		}).addTo(map);
```    
