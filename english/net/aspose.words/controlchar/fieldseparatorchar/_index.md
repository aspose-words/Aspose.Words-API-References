---
title: ControlChar.FieldSeparatorChar
linktitle: FieldSeparatorChar
articleTitle: FieldSeparatorChar
second_title: Aspose.Words for .NET
description: Discover how the ControlChar FieldSeparatorChar enhances data management by effectively separating field codes from values, optimizing your workflow effortlessly.
type: docs
weight: 90
url: /net/aspose.words/controlchar/fieldseparatorchar/
---
## ControlChar.FieldSeparatorChar field

Field separator character separates field code from field value. Optional in some fields. Value: (char)20.

```csharp
public const char FieldSeparatorChar;
```

## Examples

Shows how to add various control characters to a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add a regular space.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// Add an NBSP, which is a non-breaking space.
// Unlike the regular space, this space cannot have an automatic line break at its position.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// Add a tab character.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// Add a line break.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// Add a new line and starts a new paragraph.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// The line feed character has two versions.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// Carriage returns and line feeds can be represented together by one character.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// Add a paragraph break, which will start a new paragraph.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Add a section break. This does not make a new section or paragraph.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// Add a page break.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// A page break is the same value as a section break.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// Insert a new section, and then set its column count to two.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// We can use a control character to mark the point where text moves to the next column.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// There are char and string counterparts for most characters.
Assert.AreEqual(Convert.ToChar(ControlChar.Cell), ControlChar.CellChar);
Assert.AreEqual(Convert.ToChar(ControlChar.NonBreakingSpace), ControlChar.NonBreakingSpaceChar);
Assert.AreEqual(Convert.ToChar(ControlChar.Tab), ControlChar.TabChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineBreak), ControlChar.LineBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineFeed), ControlChar.LineFeedChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ParagraphBreak), ControlChar.ParagraphBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.SectionBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.PageBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ColumnBreak), ControlChar.ColumnBreakChar);
```

### See Also

* class [ControlChar](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
