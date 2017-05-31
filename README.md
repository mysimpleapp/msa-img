# msa-img
MySimpleApp component for image manipulation.

## CLIENT API

The following code is available by importing the corresponding web component:
```html
<!-- Example -->
<link rel="import" href="../msa-img/msa-img-selector.html"></link>
```

### Function: MsaImg.popupImgSelector
From `msa-img-selector.html`

Open popup panel allowing to select an image from computer or internet.

![Example](/doc/msa-img-selector.png)

```javascript
MsaImg.popupImgSelector(function(imgSelection){
	var src = imgSelection.src, file = imgSelection.file
	if(src) console.log("User selected image with src:", src)
	else if(file) console.log("User selected this image:", file)
})
```

* __MsaImg.popupImgSelector__: `Function(onSelect) -> popup`
  * __onSelect__: `Function(imgSelection)`, callback function called when user select an image.
    * __imgSelection__: `Object`, resulting object detqilling user selection. It can contain the folloxing attributes:
      * __src__: Image URL (if user selected an image from internet).
      * __file__: Image file (if user selected an image from computer).
  * __popup__: `HTML Element`, generated popup.

## LICENSE
MIT