---
title: ParagraphFormat.StyleIdentifier
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Ruft die gebietsschemaunabhängige Stilkennung des auf diese Formatierung angewendeten Absatzstils ab oder legt ihn fest.
type: docs
weight: 340
url: /de/net/aspose.words/paragraphformat/styleidentifier/
---
## ParagraphFormat.StyleIdentifier property

Ruft die gebietsschemaunabhängige Stilkennung des auf diese Formatierung angewendeten Absatzstils ab oder legt ihn fest.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### Beispiele

Zeigt, wie Sie ein Inhaltsverzeichnis (TOC) in ein Dokument einfügen, indem Sie Überschriftenstile als Einträge verwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein Inhaltsverzeichnis für die erste Seite des Dokuments einfügen.
// Konfigurieren Sie die Tabelle, um Absätze mit Überschriften der Ebenen 1 bis 3 aufzunehmen.
// Legen Sie außerdem seine Einträge als Hyperlinks fest, die uns führen
// an die Position der Überschrift, wenn in Microsoft Word mit der linken Maustaste geklickt wird.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Füllen Sie das Inhaltsverzeichnis, indem Sie Absätze mit Überschriftenstilen hinzufügen.
// Jede solche Überschrift mit einer Ebene zwischen 1 und 3 erstellt einen Eintrag in der Tabelle.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Ein Inhaltsverzeichnis ist ein Feld eines Typs, der aktualisiert werden muss, um ein aktuelles Ergebnis anzuzeigen.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Siehe auch

* enum [StyleIdentifier](../../styleidentifier/)
* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


