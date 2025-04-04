---
title: SdtType enumeration
linktitle: SdtType enumeration
articleTitle: SdtType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Markup.SdtType enumeration. Specifies the type of a structured document tag (SDT) node."
type: docs
weight: 150
url: /nodejs-net/aspose.words.markup/sdttype/
---

## SdtType enumeration

Specifies the type of a structured document tag (SDT) node.


### Members

| Name | Description |
| --- | --- |
| None | No type is assigned to the SDT. |
| Bibliography | The SDT represents a bibliography entry. |
| Citation | The SDT represents a citation. |
| Equation | The SDT represents an equation. |
| DropDownList | The SDT represents a drop down list when displayed in the document. |
| ComboBox | The SDT represents a combo box when displayed in the document. |
| Date | The SDT represents a date picker when displayed in the document. |
| BuildingBlockGallery | The SDT represents a building block gallery type. |
| DocPartObj | The SDT represents a document part type. |
| Group | The SDT represents a restricted grouping when displayed in the document. |
| Picture | The SDT represents a picture when displayed in the document. |
| RichText | The SDT represents a rich text box when displayed in the document. |
| PlainText | The SDT represents a plain text box when displayed in the document. |
| Checkbox | The SDT represents a checkbox when displayed in the document. |
| RepeatingSection | The SDT represents repeating section type when displayed in the document. |
| RepeatingSectionItem | The SDT represents repeating section item. |
| EntityPicker | The SDT represents an entity picker that allows the user to select an instance of an external content type. |

### Examples

Shows how to work with styles for content control elements.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are two ways to apply a style from the document to a structured document tag.
// 1 -  Apply a style object from the document's style collection:
let quoteStyle = doc.styles.at(aw.StyleIdentifier.Quote);
let sdtPlainText = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Inline);
sdtPlainText.style = quoteStyle;

// 2 -  Reference a style in the document by name:
let sdtRichText = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.RichText, aw.Markup.MarkupLevel.Inline);
sdtRichText.styleName = "Quote";

builder.insertNode(sdtPlainText);
builder.insertNode(sdtRichText);

expect(sdtPlainText.nodeType).toEqual(aw.NodeType.StructuredDocumentTag);

let tags = doc.getChildNodes(aw.NodeType.StructuredDocumentTag, true);

for (let node of tags)
{
  let sdt = node.asStructuredDocumentTag();

  console.log(sdt.wordOpenXMLMinimal);

  expect(sdt.style.styleIdentifier).toEqual(aw.StyleIdentifier.Quote);
  expect(sdt.styleName).toEqual("Quote");
}
```

Shows how to fill a table with data from in an XML part.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let xmlPart = doc.customXmlParts.add("Books",
  "<books>" +
    "<book>" +
      "<title>Everyday Italian</title>" +
      "<author>Giada De Laurentiis</author>" +
    "</book>" +
    "<book>" +
      "<title>The C Programming Language</title>" +
      "<author>Brian W. Kernighan, Dennis M. Ritchie</author>" +
    "</book>" +
    "<book>" +
      "<title>Learning XML</title>" +
      "<author>Erik T. Ray</author>" +
    "</book>" +
  "</books>");

// Create headers for data from the XML content.
let table = builder.startTable();
builder.insertCell();
builder.write("Title");
builder.insertCell();
builder.write("Author");
builder.endRow();
builder.endTable();

// Create a table with a repeating section inside.
let repeatingSectionSdt = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.RepeatingSection, aw.Markup.MarkupLevel.Row);
repeatingSectionSdt.xmlMapping.setMapping(xmlPart, "/books[1]/book", '');
table.appendChild(repeatingSectionSdt);

// Add repeating section item inside the repeating section and mark it as a row.
// This table will have a row for each element that we can find in the XML document
// using the "/books[1]/book" XPath, of which there are three.
let repeatingSectionItemSdt = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.RepeatingSectionItem, aw.Markup.MarkupLevel.Row);
repeatingSectionSdt.appendChild(repeatingSectionItemSdt);

let row = new aw.Tables.Row(doc);
repeatingSectionItemSdt.appendChild(row);

// Map XML data with created table cells for the title and author of each book.
let titleSdt = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Cell);
titleSdt.xmlMapping.setMapping(xmlPart, "/books[1]/book[1]/title[1]", '');
row.appendChild(titleSdt);

let authorSdt = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Cell);
authorSdt.xmlMapping.setMapping(xmlPart, "/books[1]/book[1]/author[1]", '');
row.appendChild(authorSdt);

doc.save(base.artifactsDir + "StructuredDocumentTag.repeatingSectionItem.docx");
```

Shows how to create group structured document tag at the Row level.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();

// Create a Group structured document tag at the Row level.
let groupSdt = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.Group, aw.Markup.MarkupLevel.Row);
table.appendChild(groupSdt);
groupSdt.isShowingPlaceholderText = false;
groupSdt.removeAllChildren();

// Create a child row of the structured document tag.
let row = new aw.Tables.Row(doc);
groupSdt.appendChild(row);

let cell = new aw.Tables.Cell(doc);
row.appendChild(cell);

builder.endTable();

// Insert cell contents.
cell.ensureMinimum();
builder.moveTo(cell.lastParagraph);
builder.write("Lorem ipsum dolor.");

// Insert text after the table.
builder.moveTo(table.nextSibling);
builder.write("Nulla blandit nisi.");

doc.save(base.artifactsDir + "StructuredDocumentTag.SdtAtRowLevel.docx");
```

Shows how to create a structured document tag of the Citation type.

```js
let doc = new aw.Document();

let sdt = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.Citation, aw.Markup.MarkupLevel.Inline);
let paragraph = doc.firstSection.body.firstParagraph;
paragraph.appendChild(sdt);

// Create a Citation field.
let builder = new aw.DocumentBuilder(doc);
builder.moveToParagraph(0, -1);
builder.insertField(String.raw`CITATION Ath22 \l 1033 `, "(John Lennon, 2022)");

// Move the field to the structured document tag.
while (sdt.nextSibling != null)
  sdt.appendChild(sdt.nextSibling);

doc.save(base.artifactsDir + "StructuredDocumentTag.citation.docx");
```

### See Also

* module [Aspose.Words.Markup](../)

