---
title: ControlChar.CrLf
linktitle: CrLf
articleTitle: CrLf
second_title: Aspose.Words für .NET
description: ControlChar CrLf veld. Wagenrücklauf gefolgt von einem Zeilenvorschubzeichen x000dx000a oder rn. Wird als solches nicht in Microsoft WordDokumenten verwendet wird aber häufig in Textdateien für Absatzumbrüche verwendet in C#.
type: docs
weight: 60
url: /de/net/aspose.words/controlchar/crlf/
---
## ControlChar.CrLf field

Wagenrücklauf, gefolgt von einem Zeilenvorschubzeichen: „\x000d\x000a“ oder „\r\n“. Wird als solches nicht in Microsoft Word-Dokumenten verwendet, wird aber häufig in Textdateien für Absatzumbrüche verwendet.

```csharp
public static readonly string CrLf;
```

## Beispiele

Zeigt, wie man einem Dokument verschiedene Steuerzeichen hinzufügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein reguläres Leerzeichen hinzufügen.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// Fügen Sie ein NBSP hinzu, bei dem es sich um ein geschütztes Leerzeichen handelt.
// Im Gegensatz zum regulären Leerzeichen kann dieses Leerzeichen an seiner Position keinen automatischen Zeilenumbruch haben.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// Tabulatorzeichen hinzufügen.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// Zeilenumbruch hinzufügen.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// Eine neue Zeile hinzufügen und einen neuen Absatz beginnen.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Das Zeilenvorschubzeichen hat zwei Versionen.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// Wagenrücklauf und Zeilenvorschub können gemeinsam durch ein Zeichen dargestellt werden.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// Einen Absatzumbruch hinzufügen, der einen neuen Absatz beginnt.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Einen Abschnittsumbruch hinzufügen. Dadurch wird kein neuer Abschnitt oder Absatz erstellt.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// Einen Seitenumbruch hinzufügen.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// Ein Seitenumbruch hat denselben Wert wie ein Abschnittsumbruch.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// Einen neuen Abschnitt einfügen und dann seine Spaltenanzahl auf zwei setzen.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// Wir können ein Steuerzeichen verwenden, um den Punkt zu markieren, an dem der Text in die nächste Spalte wechselt.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// Für die meisten Zeichen gibt es char- und string-Gegenstücke.
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
