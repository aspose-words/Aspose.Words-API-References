---
title: Paragraph.BreakIsStyleSeparator
second_title: Aspose.Words für .NET-API-Referenz
description: Paragraph eigendom. True wenn dieser Absatzumbruch ein Stiltrennzeichen ist. Ein Stiltrennzeichen ermöglicht dass ein Absatz aus Teilen mit unterschiedlichen Absatzstilen bestehen kann.
type: docs
weight: 20
url: /de/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

True, wenn dieser Absatzumbruch ein Stiltrennzeichen ist. Ein Stiltrennzeichen ermöglicht, dass ein Absatz aus Teilen mit unterschiedlichen Absatzstilen bestehen kann.

```csharp
public bool BreakIsStyleSeparator { get; }
```

### Beispiele

Zeigt, wie man Text in dieselbe Zeile wie die Überschrift eines Inhaltsverzeichnisses schreibt und dafür sorgt, dass dieser nicht im Inhaltsverzeichnis angezeigt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Einen Absatz mit einem Stil einfügen, den das Inhaltsverzeichnis als Eintrag aufnimmt.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// Diese beiden Zeichenfolgen befinden sich im selben Absatz und werden daher im selben TOC-Eintrag angezeigt.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// Wenn wir ein Stiltrennzeichen einfügen, können wir mehr Text in denselben Absatz schreiben
// und einen anderen Stil verwenden, ohne dass dieser im Inhaltsverzeichnis angezeigt wird.
// Wenn wir nach dem Trennzeichen einen Überschriftenstil verwenden, können wir mehrere Inhaltsverzeichniseinträge aus einer Dokumenttextzeile zeichnen.
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### Siehe auch

* class [Paragraph](../)
* namensraum [Aspose.Words](../../paragraph/)
* Montage [Aspose.Words](../../../)


