---
title: Paragraph.BreakIsStyleSeparator
linktitle: BreakIsStyleSeparator
articleTitle: BreakIsStyleSeparator
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „Absatzumbruch IsStyleSeparator“ die Dokumentformatierung verbessert, indem sie gemischte Absatzstile für mehr Designflexibilität ermöglicht.
type: docs
weight: 20
url: /de/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

Wahr, wenn dieser Absatzumbruch ein Stiltrennzeichen ist. Ein Stiltrennzeichen ermöglicht es, dass ein Absatz aus Teilen mit unterschiedlichen Absatzstilen besteht.

```csharp
public bool BreakIsStyleSeparator { get; }
```

## Beispiele

Zeigt, wie Sie Text in dieselbe Zeile wie eine Inhaltsverzeichnisüberschrift schreiben, ohne dass er im Inhaltsverzeichnis angezeigt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Fügen Sie einen Absatz mit einem Stil ein, den das Inhaltsverzeichnis als Eintrag übernimmt.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// Beide Zeichenfolgen befinden sich im selben Absatz und werden daher im selben Inhaltsverzeichniseintrag angezeigt.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// Wenn wir einen Stiltrenner einfügen, können wir mehr Text in den gleichen Absatz schreiben
// und einen anderen Stil verwenden, ohne im Inhaltsverzeichnis angezeigt zu werden.
// Wenn wir nach dem Trennzeichen einen Überschriftenstil verwenden, können wir aus einer Dokumenttextzeile mehrere Inhaltsverzeichniseinträge zeichnen.
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### Siehe auch

* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
