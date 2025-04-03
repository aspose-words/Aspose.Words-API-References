---
title: HtmlSaveOptions.exportTextInputFormFieldAsText property
linktitle: exportTextInputFormFieldAsText property
articleTitle: exportTextInputFormFieldAsText property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.exportTextInputFormFieldAsText property. Controls how text input form fields are saved to HTML or MHTML"
type: docs
weight: 260
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/exportTextInputFormFieldAsText/
---

## HtmlSaveOptions.exportTextInputFormFieldAsText property

Controls how text input form fields are saved to HTML or MHTML.
Default value is ``false``.



```js
get exportTextInputFormFieldAsText(): boolean
```

### Remarks

When set to ``true``, exports text input form fields as normal text. 
When ``false``, exports Word text input form fields as INPUT elements in HTML.

When exporting to EPUB, text input form fields are always saved as text due 
to requirements of this format.




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

