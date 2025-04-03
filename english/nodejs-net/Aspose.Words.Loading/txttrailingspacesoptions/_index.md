---
title: TxtTrailingSpacesOptions enumeration
linktitle: TxtTrailingSpacesOptions enumeration
articleTitle: TxtTrailingSpacesOptions enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Loading.TxtTrailingSpacesOptions enumeration. Specifies available options for trailing spaces handling during import from [LoadFormat.Text](../../aspose.words/loadformat/#Text) file."
type: docs
weight: 200
url: /nodejs-net/Aspose.Words.Loading/txttrailingspacesoptions/
---

## TxtTrailingSpacesOptions enumeration

Specifies available options for trailing spaces handling during import from [LoadFormat.Text](../../aspose.words/loadformat/#Text) file.



### Members

| Name | Description |
| --- | --- |
| Trim | Trailing spaces are trimmed. |
| Preserve | Trailing spaces are preserved. |

### Examples

Shows how to trim whitespace when loading plaintext documents.

```js
const textDoc = "      Line 1 \n" +
        "    Line 2   \n" +
        " Line 3       ";

// Create a "TxtLoadOptions" object, which we can pass to a document's constructor
// to modify how we load a plaintext document.
let loadOptions = new aw.Loading.TxtLoadOptions();

// Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
// to preserve all whitespace characters at the start of every line.
// Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
// to remove all whitespace characters from the start of every line,
// and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
// Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
// to remove all whitespace characters from every line's start.
loadOptions.leadingSpacesOptions = txtLeadingSpacesOptions;

// Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
// to preserve all whitespace characters at the end of every line. 
// Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to 
// remove all whitespace characters from the end of every line.
loadOptions.trailingSpacesOptions = txtTrailingSpacesOptions;

let doc = new aw.Document(Buffer.from(textDoc), loadOptions);
let paragraphs = doc.firstSection.body.paragraphs.toArray();

switch (txtLeadingSpacesOptions)
{
  case aw.Loading.TxtLeadingSpacesOptions.ConvertToIndent:
    expect(paragraphs[0].paragraphFormat.firstLineIndent).toEqual(37.8);
    expect(paragraphs[1].paragraphFormat.firstLineIndent).toEqual(25.2);
    expect(paragraphs[2].paragraphFormat.firstLineIndent).toEqual(6.3);

    expect(paragraphs[0].getText().startsWith("Line 1")).toEqual(true);
    expect(paragraphs[1].getText().startsWith("Line 2")).toEqual(true);
    expect(paragraphs[2].getText().startsWith("Line 3")).toEqual(true);
    break;
  case aw.Loading.TxtLeadingSpacesOptions.Preserve:
    expect(paragraphs.every(p => p.paragraphFormat.firstLineIndent == 0.0)).toEqual(true);

    expect(paragraphs[0].getText().startsWith("      Line 1")).toEqual(true);
    expect(paragraphs[1].getText().startsWith("    Line 2")).toEqual(true);
    expect(paragraphs[2].getText().startsWith(" Line 3")).toEqual(true);
    break;
  case aw.Loading.TxtLeadingSpacesOptions.Trim:
    expect(paragraphs.every(p => p.paragraphFormat.firstLineIndent == 0.0)).toEqual(true);

    expect(paragraphs[0].getText().startsWith("Line 1")).toEqual(true);
    expect(paragraphs[1].getText().startsWith("Line 2")).toEqual(true);
    expect(paragraphs[2].getText().startsWith("Line 3")).toEqual(true);
    break;
}

switch (txtTrailingSpacesOptions)
{
  case aw.Loading.TxtTrailingSpacesOptions.Preserve:
    expect(paragraphs[0].getText().endsWith("Line 1 \r")).toEqual(true);
    expect(paragraphs[1].getText().endsWith("Line 2   \r")).toEqual(true);
    expect(paragraphs[2].getText().endsWith("Line 3       \f")).toEqual(true);
    break;
  case aw.Loading.TxtTrailingSpacesOptions.Trim:
    expect(paragraphs[0].getText().endsWith("Line 1\r")).toEqual(true);
    expect(paragraphs[1].getText().endsWith("Line 2\r")).toEqual(true);
    expect(paragraphs[2].getText().endsWith("Line 3\f")).toEqual(true);
    break;
}
```

### See Also

* module [Aspose.Words.Loading](../)

