---
title: HtmlSaveOptions.exportDropDownFormFieldAsText property
linktitle: exportDropDownFormFieldAsText property
articleTitle: exportDropDownFormFieldAsText property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.exportDropDownFormFieldAsText property. Controls how drop-down form fields are saved to HTML or MHTML"
type: docs
weight: 130
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/exportDropDownFormFieldAsText/
---

## HtmlSaveOptions.exportDropDownFormFieldAsText property

Controls how drop-down form fields are saved to HTML or MHTML.
Default value is ``false``.



```js
get exportDropDownFormFieldAsText(): boolean
```

### Remarks

When set to ``true``, exports drop-down form fields as normal text.
When ``false``, exports drop-down form fields as SELECT element in HTML.

When exporting to EPUB, text drop-down form fields are always saved as text due
to requirements of this format.




### Examples

Shows how to get drop-down combo box form fields to blend in with paragraph text when saving to html.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Use a document builder to insert a combo box with the value "Two" selected.
builder.insertComboBox("MyComboBox", [ "One", "Two", "Three" ], 1);

// The "ExportDropDownFormFieldAsText" flag of this SaveOptions object allows us to
// control how saving the document to HTML treats drop-down combo boxes.
// Setting it to "true" will convert each combo box into simple text
// that displays the combo box's currently selected value, effectively freezing it.
// Setting it to "false" will preserve the functionality of the combo box using <select> and <option> tags.
let options = new aw.Saving.HtmlSaveOptions();
options.exportDropDownFormFieldAsText = exportDropDownFormFieldAsText;    

doc.save(base.artifactsDir + "HtmlSaveOptions.DropDownFormField.html", options);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.DropDownFormField.html").toString();

if (exportDropDownFormFieldAsText)
  expect(outDocContents.includes("<span>Two</span>")).toBe(true);
else
  expect(outDocContents.includes(
    "<select name=\"MyComboBox\">" +
      "<option>One</option>" +
      "<option selected=\"selected\">Two</option>" +
      "<option>Three</option>" +
    "</select>")).toBe(true);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

