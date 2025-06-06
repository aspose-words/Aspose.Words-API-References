---
title: ControlChar.CellChar
linktitle: CellChar
articleTitle: CellChar
second_title: Aspose.Words für .NET
description: Entdecken Sie das ControlChar CellChar-Feld für nahtlose Tabellenverwaltung. Verbessern Sie Ihre Datenorganisation mit effizienten Zellen- und Zeilenendezeichen.
type: docs
weight: 20
url: /de/net/aspose.words/controlchar/cellchar/
---
## ControlChar.CellChar field

Ende einer Tabellenzelle oder Ende einer Tabellenzeile Zeichen: (char)7 oder "\a".

```csharp
public const char CellChar;
```

## Beispiele

Zeigt, wie einem Dokument verschiedene Steuerzeichen hinzugefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein normales Leerzeichen hinzu.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// Fügen Sie ein NBSP hinzu, ein geschütztes Leerzeichen.
// Anders als beim normalen Leerzeichen kann an dieser Stelle kein automatischer Zeilenumbruch erfolgen.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// Ein Tabulatorzeichen hinzufügen.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// Einen Zeilenumbruch hinzufügen.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// Fügt eine neue Zeile hinzu und beginnt einen neuen Absatz.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Das Zeilenvorschubzeichen hat zwei Versionen.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// Wagenrückläufe und Zeilenvorschübe können zusammen durch ein Zeichen dargestellt werden.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// Fügen Sie einen Absatzumbruch hinzu, der einen neuen Absatz beginnt.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Einen Abschnittsumbruch hinzufügen. Dadurch wird kein neuer Abschnitt oder Absatz erstellt.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// Einen Seitenumbruch hinzufügen.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// Ein Seitenumbruch hat den gleichen Wert wie ein Abschnittsumbruch.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// Fügen Sie einen neuen Abschnitt ein und legen Sie dann die Spaltenanzahl auf zwei fest.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// Wir können ein Steuerzeichen verwenden, um den Punkt zu markieren, an dem der Text in die nächste Spalte verschoben wird.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// Für die meisten Zeichen gibt es Char- und String-Gegenstücke.
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

### Siehe auch

* class [ControlChar](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
