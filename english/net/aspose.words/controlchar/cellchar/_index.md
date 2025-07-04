---
title: ControlChar.CellChar
linktitle: CellChar
articleTitle: CellChar
second_title: Aspose.Words for .NET
description: Discover the ControlChar CellChar field for seamless table management. Enhance your data organization with efficient end-of-cell and row characters.
type: docs
weight: 20
url: /net/aspose.words/controlchar/cellchar/
---
## ControlChar.CellChar field

End of a table cell or end of a table row character: (char)7 or "\a".

```csharp
public const char CellChar;
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
Assert.That(doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count, Is.EqualTo(1));
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.That(doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count, Is.EqualTo(2));

// The line feed character has two versions.
Assert.That(ControlChar.Lf, Is.EqualTo(ControlChar.LineFeed));

// Carriage returns and line feeds can be represented together by one character.
Assert.That(ControlChar.Cr + ControlChar.Lf, Is.EqualTo(ControlChar.CrLf));

// Add a paragraph break, which will start a new paragraph.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.That(doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count, Is.EqualTo(3));

// Add a section break. This does not make a new section or paragraph.
Assert.That(doc.Sections.Count, Is.EqualTo(1));
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.That(doc.Sections.Count, Is.EqualTo(1));

// Add a page break.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// A page break is the same value as a section break.
Assert.That(ControlChar.SectionBreak, Is.EqualTo(ControlChar.PageBreak));

// Insert a new section, and then set its column count to two.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// We can use a control character to mark the point where text moves to the next column.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// There are char and string counterparts for most characters.
Assert.That(ControlChar.CellChar, Is.EqualTo(Convert.ToChar(ControlChar.Cell)));
Assert.That(ControlChar.NonBreakingSpaceChar, Is.EqualTo(Convert.ToChar(ControlChar.NonBreakingSpace)));
Assert.That(ControlChar.TabChar, Is.EqualTo(Convert.ToChar(ControlChar.Tab)));
Assert.That(ControlChar.LineBreakChar, Is.EqualTo(Convert.ToChar(ControlChar.LineBreak)));
Assert.That(ControlChar.LineFeedChar, Is.EqualTo(Convert.ToChar(ControlChar.LineFeed)));
Assert.That(ControlChar.ParagraphBreakChar, Is.EqualTo(Convert.ToChar(ControlChar.ParagraphBreak)));
Assert.That(ControlChar.SectionBreakChar, Is.EqualTo(Convert.ToChar(ControlChar.SectionBreak)));
Assert.That(ControlChar.SectionBreakChar, Is.EqualTo(Convert.ToChar(ControlChar.PageBreak)));
Assert.That(ControlChar.ColumnBreakChar, Is.EqualTo(Convert.ToChar(ControlChar.ColumnBreak)));
```

### See Also

* class [ControlChar](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
