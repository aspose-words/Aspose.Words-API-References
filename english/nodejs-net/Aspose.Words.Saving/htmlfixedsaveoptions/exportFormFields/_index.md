---
title: HtmlFixedSaveOptions.exportFormFields property
linktitle: exportFormFields property
articleTitle: exportFormFields property
second_title: Aspose.Words for NodeJs
description: "HtmlFixedSaveOptions.exportFormFields property. Gets or sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics."
type: docs
weight: 80
url: /nodejs-net/aspose.words.saving/htmlfixedsaveoptions/exportFormFields/
---

## HtmlFixedSaveOptions.exportFormFields property

Gets or sets indication of whether form fields are exported as interactive
items (as 'input' tag) rather than converted to text or graphics.


```js
get exportFormFields(): boolean
```

### Examples

Shows how to export form fields to Html.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertCheckBox("CheckBox", false, 15);

// When we export a document with form fields to .html,
// there are two ways in which Aspose.words can export form fields.
// Setting the "ExportFormFields" flag to "true" will export them as interactive objects.
// Setting this flag to "false" will display form fields as plain text.
// This will freeze them at their current value, and prevent the reader of our HTML document
// from being able to interact with them.
let htmlFixedSaveOptions = new aw.Saving.HtmlFixedSaveOptions();
htmlFixedSaveOptions.exportFormFields = exportFormFields;

doc.save(base.artifactsDir + "HtmlFixedSaveOptions.exportFormFields.html", htmlFixedSaveOptions);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlFixedSaveOptions.exportFormFields.html").toString();

if (exportFormFields)
{
  expect(outDocContents.includes("<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
    "<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />")).toBeTruthy();
}
else
{
  expect(outDocContents.includes("<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
    "<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"")).toBeTruthy();
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)

