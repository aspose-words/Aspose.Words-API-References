---
title: HtmlSaveOptions.exportXhtmlTransitional property
linktitle: exportXhtmlTransitional property
articleTitle: exportXhtmlTransitional property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.exportXhtmlTransitional property. Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML"
type: docs
weight: 280
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/exportXhtmlTransitional/
---

## HtmlSaveOptions.exportXhtmlTransitional property

Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML.
When ``true``, writes a DOCTYPE declaration in the document prior to the root element.
Default value is ``false``.
When saving to EPUB or HTML5 ([HtmlVersion.Html5](../../htmlversion/#Html5)) the DOCTYPE
declaration is always written.



```js
get exportXhtmlTransitional(): boolean
```

### Remarks

Aspose.Words always writes well formed HTML regardless of this setting.

When ``true``, the beginning of the HTML output document will look like this:

```

<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html
      PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">

```
Aspose.Words aims to output XHTML according to the XHTML 1.0 Transitional specification,
but the output will not always validate against the DTD. Some structures inside a Microsoft Word
document are hard or impossible to map to a document that will validate against the XHTML schema.
For example, XHTML does not allow nested lists (UL cannot be nested inside another UL element),
but in Microsoft Word document multilevel lists occur quite often.




### Examples

Shows how to display a DOCTYPE heading when converting documents to the Xhtml 1.0 transitional standard.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");

let options = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Html);
options.htmlVersion = aw.Saving.HtmlVersion.Xhtml;
options.exportXhtmlTransitional = showDoctypeDeclaration;
options.prettyFormat = true;

doc.save(base.artifactsDir + "HtmlSaveOptions.exportXhtmlTransitional.html", options);

// Our document will only contain a DOCTYPE declaration heading if we have set the "ExportXhtmlTransitional" flag to "true".
let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.exportXhtmlTransitional.html").toString();

if (showDoctypeDeclaration)
  expect(outDocContents.includes(
    "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n" +
    "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
    "<html xmlns=\"http://www.w3.org/1999/xhtml\">")).toEqual(true);
else
  expect(outDocContents.includes("<html>")).toEqual(true);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

