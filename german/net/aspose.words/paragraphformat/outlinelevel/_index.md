---
title: OutlineLevel
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt die Gliederungsebene des Absatzes im Dokument an.
type: docs
weight: 240
url: /de/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Gibt die Gliederungsebene des Absatzes im Dokument an.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

### Beispiele

Zeigt, wie Absatzgliederungsebenen konfiguriert werden, um reduzierbaren Text zu erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Jeder Absatz hat einen OutlineLevel, der eine beliebige Zahl von 1 bis 9 sein kann, oder den Standardwert "BodyText".
// Wenn Sie die Eigenschaft auf einen der nummerierten Werte setzen, wird ein Pfeil nach links angezeigt
// des Absatzanfangs.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Ebene 1 ist die oberste Ebene. Befindet sich ein Absatz mit einer niedrigeren Ebene unter einem Absatz mit einer höheren Ebene,
// das Reduzieren des Absatzes auf höherer Ebene wird den Absatz auf niedrigerer Ebene reduzieren.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Zwei Absätze der gleichen Ebene werden nicht zusammengeklappt,
// und die Pfeile reduzieren nicht die Absätze, auf die sie zeigen.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Der Standardwert "BodyText" ist der niedrigste, den ein Absatz auf jeder Ebene reduzieren kann.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Siehe auch

* enum [OutlineLevel](../../outlinelevel)
* class [ParagraphFormat](../../paragraphformat)
* namensraum [Aspose.Words](../../paragraphformat)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
