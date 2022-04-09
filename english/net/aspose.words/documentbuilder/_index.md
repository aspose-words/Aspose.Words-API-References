---
title: DocumentBuilder
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 430
url: /net/aspose.words/documentbuilder/
---
## DocumentBuilder class

Provides methods to insert text, images and other content, specify font, paragraph and section formatting.

```csharp
public class DocumentBuilder
```

## Public Members

| name | description |
| --- | --- |
| [DocumentBuilder](documentbuilder)() | Initializes a new instance of this class. |
| [DocumentBuilder](documentbuilder)(…) | Initializes a new instance of this class. |
| [Bold](bold) { get; set; } | True if the font is formatted as bold. |
| [CellFormat](cellformat) { get; } | Returns an object that represents current table cell formatting properties. |
| [CurrentNode](currentnode) { get; } | Gets the node that is currently selected in this DocumentBuilder. |
| [CurrentParagraph](currentparagraph) { get; } | Gets the paragraph that is currently selected in this DocumentBuilder. |
| [CurrentSection](currentsection) { get; } | Gets the section that is currently selected in this DocumentBuilder. |
| [CurrentStory](currentstory) { get; } | Gets the story that is currently selected in this DocumentBuilder. |
| [Document](document) { get; set; } | Gets or sets the [`Document`](./document) object that this object is attached to. |
| [Font](font) { get; } | Returns an object that represents current font formatting properties. |
| [IsAtEndOfParagraph](isatendofparagraph) { get; } | Returns true if the cursor is at the end of the current paragraph. |
| [IsAtStartOfParagraph](isatstartofparagraph) { get; } | Returns true if the cursor is at the beginning of the current paragraph (no text before the cursor). |
| [Italic](italic) { get; set; } | True if the font is formatted as italic. |
| [ListFormat](listformat) { get; } | Returns an object that represents current list formatting properties. |
| [PageSetup](pagesetup) { get; } | Returns an object that represents current page setup and section properties. |
| [ParagraphFormat](paragraphformat) { get; } | Returns an object that represents current paragraph formatting properties. |
| [RowFormat](rowformat) { get; } | Returns an object that represents current table row formatting properties. |
| [Underline](underline) { get; set; } | Gets/sets underline type for the current font. |
| [DeleteRow](deleterow)(…) | Deletes a row from a table. |
| [EndBookmark](endbookmark)(…) | Marks the current position in the document as a bookmark end. |
| [EndColumnBookmark](endcolumnbookmark)(…) | Marks the current position in the document as a column bookmark end. The position must be in a table cell. |
| [EndEditableRange](endeditablerange)() | Marks the current position in the document as an editable range end. |
| [EndEditableRange](endeditablerange)(…) | Marks the current position in the document as an editable range end. |
| [EndRow](endrow)() | Ends a table row in the document. |
| [EndTable](endtable)() | Ends a table in the document. |
| [InsertBreak](insertbreak)(…) | Inserts a break of the specified type into the document. |
| [InsertCell](insertcell)() | Inserts a table cell into the document. |
| [InsertChart](insertchart)(…) | Inserts an chart object into the document and scales it to the specified size. (2 methods) |
| [InsertCheckBox](insertcheckbox)(…) | Inserts a checkbox form field at the current position. (2 methods) |
| [InsertComboBox](insertcombobox)(…) | Inserts a combobox form field at the current position. |
| [InsertDocument](insertdocument)(…) | Inserts a document at the cursor position. (2 methods) |
| [InsertField](insertfield)(…) | Inserts a Word field into a document and optionally updates the field result. (3 methods) |
| [InsertFootnote](insertfootnote)(…) | Inserts a footnote or endnote into the document. (2 methods) |
| [InsertHorizontalRule](inserthorizontalrule)() | Inserts a horizontal rule shape into the document. |
| [InsertHtml](inserthtml)(…) | Inserts an HTML string into the document. (3 methods) |
| [InsertHyperlink](inserthyperlink)(…) | Inserts a hyperlink into the document. |
| [InsertImage](insertimage)(…) |  (12 methods) |
| [InsertNode](insertnode)(…) | Inserts a text level node inside the current paragraph before the cursor. |
| [InsertOleObject](insertoleobject)(…) | Inserts an embedded OLE object from a stream into the document. (3 methods) |
| [InsertOleObjectAsIcon](insertoleobjectasicon)(…) | Inserts an embedded or linked OLE object as icon into the document. Allows to specify icon file and caption. Detects OLE object type using file extension. (3 methods) |
| [InsertOnlineVideo](insertonlinevideo)(…) | Inserts an online video object into the document and scales it to the specified size. (4 methods) |
| [InsertParagraph](insertparagraph)() | Inserts a paragraph break into the document. |
| [InsertShape](insertshape)(…) | Inserts inline shape with specified type and size. (2 methods) |
| [InsertSignatureLine](insertsignatureline)(…) | Inserts a signature line at the current position. (2 methods) |
| [InsertStyleSeparator](insertstyleseparator)() | Inserts style separator into the document. |
| [InsertTableOfContents](inserttableofcontents)(…) | Inserts a TOC (table of contents) field into the document. |
| [InsertTextInput](inserttextinput)(…) | Inserts a text form field at the current position. |
| [MoveTo](moveto)(…) | Moves the cursor to an inline node or to the end of a paragraph. |
| [MoveToBookmark](movetobookmark)(…) | Moves the cursor to a bookmark. (2 methods) |
| [MoveToCell](movetocell)(…) | Moves the cursor to a table cell in the current section. |
| [MoveToDocumentEnd](movetodocumentend)() | Moves the cursor to the end of the document. |
| [MoveToDocumentStart](movetodocumentstart)() | Moves the cursor to the beginning of the document. |
| [MoveToField](movetofield)(…) | Moves the cursor to a field in the document. |
| [MoveToHeaderFooter](movetoheaderfooter)(…) | Moves the cursor to the beginning of a header or footer in the current section. |
| [MoveToMergeField](movetomergefield)(…) | Moves the cursor to a position just beyond the specified merge field and removes the merge field. (2 methods) |
| [MoveToParagraph](movetoparagraph)(…) | Moves the cursor to a paragraph in the current section. |
| [MoveToSection](movetosection)(…) | Moves the cursor to the beginning of the body in a specified section. |
| [PopFont](popfont)() | Retrieves character formatting previously saved on the stack. |
| [PushFont](pushfont)() | Saves current character formatting onto the stack. |
| [StartBookmark](startbookmark)(…) | Marks the current position in the document as a bookmark start. |
| [StartColumnBookmark](startcolumnbookmark)(…) | Marks the current position in the document as a column bookmark start. The position must be in a table cell. |
| [StartEditableRange](starteditablerange)() | Marks the current position in the document as an editable range start. |
| [StartTable](starttable)() | Starts a table in the document. |
| [Write](write)(…) | Inserts a string into the document at the current insert position. |
| [Writeln](writeln)() | Inserts a paragraph break into the document. |
| [Writeln](writeln)(…) | Inserts a string and a paragraph break into the document. |

## Remarks

DocumentBuilder makes the process of building a Document easier. Document is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. DocumentBuilder is a "facade" for the complex structure of Document and allows to insert content and formatting quickly and easily.Create a DocumentBuilder and associate it with a [`Document`](./document).The DocumentBuilder has an internal cursor where the text will be inserted when you call [`Write`](./write), [`Writeln`](./writeln), [`InsertBreak`](./insertbreak) and other methods. You can navigate the DocumentBuilder cursor to a different location in a document using various MoveToXXX methods.Use the [`Font`](./font) property to specify character formatting that will apply to all text inserted from the current position in the document onwards.Use the [`ParagraphFormat`](./paragraphformat) property to specify paragraph formatting for the current and all paragraphs that will be inserted.Use the [`PageSetup`](./pagesetup) property to specify page and section properties for the current section and all section that will be inserted.Use the [`CellFormat`](./cellformat) and [`RowFormat`](./rowformat) properties to specify formatting properties for table cells and rows. User the [`InsertCell`](./insertcell) and [`EndRow`](./endrow) methods to build a table.Note that Font, ParagraphFormat and PageSetup properties are updated whenever you navigate to a different place in the document to reflect formatting properties available at the new location.

### See Also

* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
