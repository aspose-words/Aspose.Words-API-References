---
title: ParagraphFormat.OutlineLevel
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PargraphFormat OutlineLevel“, um die Absatzhierarchie in Ihren Dokumenten einfach zu definieren und so die Organisation und Lesbarkeit zu verbessern.
type: docs
weight: 260
url: /de/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Gibt die Gliederungsebene des Absatzes im Dokument an.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

## Beispiele

Zeigt, wie Sie Absatzgliederungsebenen konfigurieren, um reduzierbaren Text zu erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Jeder Absatz hat einen OutlineLevel, der eine beliebige Zahl zwischen 1 und 9 oder der Standardwert „BodyText“ sein kann.
// Wenn Sie die Eigenschaft auf einen der nummerierten Werte setzen, wird ein Pfeil nach links angezeigt
// vom Anfang des Absatzes.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Ebene 1 ist die oberste Ebene. Wenn sich unter einem Absatz mit einer höheren Ebene ein Absatz mit einer niedrigeren Ebene befindet,
// Durch das Ausblenden des Absatzes auf höherer Ebene wird auch der Absatz auf niedrigerer Ebene ausgeblendet.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Zwei Absätze derselben Ebene werden nicht zusammenfallen,
// und die Pfeile klappen die Absätze, auf die sie zeigen, nicht zusammen.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Der Standardwert für „BodyText“ ist der niedrigste, um den ein Absatz jeder Ebene eingeklappt werden kann.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Siehe auch

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
