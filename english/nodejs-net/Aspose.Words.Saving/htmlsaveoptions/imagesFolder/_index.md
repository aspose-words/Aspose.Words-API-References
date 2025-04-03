---
title: HtmlSaveOptions.imagesFolder property
linktitle: imagesFolder property
articleTitle: imagesFolder property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.imagesFolder property. Specifies the physical folder where images are saved when exporting a document to HTML format"
type: docs
weight: 360
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/imagesFolder/
---

## HtmlSaveOptions.imagesFolder property

Specifies the physical folder where images are saved when exporting a document to HTML format.
Default is an empty string.


```js
get imagesFolder(): string
```

### Remarks

When you save a [Document](../../../aspose.words/document/) in HTML format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [HtmlSaveOptions.imagesFolder](./) 
allows you to specify where the images will be saved and [HtmlSaveOptions.imagesFolderAlias](../imagesFolderAlias/) 
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the 
images in the same folder where the document file is saved. Use [HtmlSaveOptions.imagesFolder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, 
but still needs to save the images somewhere. In this case, you need to specify an accessible folder 
in the [HtmlSaveOptions.imagesFolder](./) property or provide custom streams via 
the [HtmlSaveOptions.imageSavingCallback](../imageSavingCallback/) event handler.

If the folder specified by [HtmlSaveOptions.imagesFolder](./) doesn't exist, it will be created automatically.

[HtmlSaveOptions.resourceFolder](../resourceFolder/) is another way to specify a folder where images should be saved.




### Examples

Shows how to specify the folder for storing linked images after saving to .html.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let imagesDir = path.join(base.artifactsDir, "SaveHtmlWithOptions");

if (fs.existsSync(imagesDir)) {
  fs.rmSync(imagesDir, { recursive: true, force: true });
}

fs.mkdirSync(imagesDir, { recursive: true });

// Set an option to export form fields as plain text instead of HTML input elements.
let options = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Html);
options.exportTextInputFormFieldAsText = true;
options.imagesFolder = imagesDir;

doc.save(base.artifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.resourceFolder](../resourceFolder/)
* property [HtmlSaveOptions.imagesFolderAlias](../imagesFolderAlias/)
* property [HtmlSaveOptions.imageSavingCallback](../imageSavingCallback/)

