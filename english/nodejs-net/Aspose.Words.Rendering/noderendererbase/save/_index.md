---
title: NodeRendererBase.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Rendering.NodeRendererBase.save method"
type: docs
weight: 30
url: /nodejs-net/aspose.words.rendering/noderendererbase/save/
---

## save(fileName, saveOptions) {#string_imagesaveoptions}

Renders the shape into an image and saves into a file.


```js
save(fileName: string, saveOptions: Aspose.Words.Saving.ImageSaveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The name for the image file. If a file with the specified name already exists, the existing file is overwritten. |
| saveOptions | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Specifies the options that control how the shape is rendered and saved. Can be ``null``. |

## save(fileName, saveOptions) {#string_svgsaveoptions}

Renders the shape into an SVG image and saves into a file.


```js
save(fileName: string, saveOptions: Aspose.Words.Saving.SvgSaveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The name for the image file. If a file with the specified name already exists, the existing file is overwritten. |
| saveOptions | [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/) | Specifies the options that control how the shape is rendered and saved. Can be ``null``. |

## save(stream, saveOptions) {#buffer_imagesaveoptions}

Renders the shape into an image and saves into a stream.


```js
save(stream: Buffer, saveOptions: Aspose.Words.Saving.ImageSaveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | The stream where to save the image of the shape. |
| saveOptions | [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/) | Specifies the options that control how the shape is rendered and saved. Can be ``null``. If this is ``null``, the image will be saved in the PNG format. |

## save(stream, saveOptions) {#buffer_svgsaveoptions}

Renders the shape into an SVG image and saves into a stream.


```js
save(stream: Buffer, saveOptions: Aspose.Words.Saving.SvgSaveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Buffer | The stream where to save the SVG image of the shape. |
| saveOptions | [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/) | Specifies the options that control how the shape is rendered and saved. Can be ``null``. If this is ``null``, the image will be saved with the default options. |

## Examples

Shows how to render an Office Math object into an image file in the local file system.

```js
let doc = new aw.Document(base.myDir + "Office math.docx");

let officeMath = doc.getOfficeMath(0, true);

// Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
// how it renders the OfficeMath node into an image.
let saveOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Png);

// Set the "Scale" property to 5 to render the object to five times its original size.
saveOptions.scale = 5;

officeMath.getMathRenderer().save(base.artifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

Shows how to pass save options when rendering office math.

```js
let doc = new aw.Document(base.myDir + "Office math.docx");

let math = doc.getOfficeMath(0, true);

let options = new aw.Saving.SvgSaveOptions();
options.textOutputMode = aw.Saving.SvgTextOutputMode.UsePlacedGlyphs;

math.getMathRenderer().save(base.artifactsDir + "SvgSaveOptions.Output.svg", options);
```

## See Also

* module [Aspose.Words.Rendering](../../)
* class [NodeRendererBase](../)

