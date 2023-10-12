---
title: ParagraphFormat.OutlineLevel
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Gibt die Gliederungsebene des Absatzes im Dokument an.
type: docs
weight: 250
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

// Jeder Absatz hat einen OutlineLevel, der eine beliebige Zahl von 1 bis 9 oder den Standardwert „BodyText“ sein kann.
// Wenn Sie die Eigenschaft auf einen der nummerierten Werte setzen, wird ein Pfeil nach links angezeigt
// vom Anfang des Absatzes.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Ebene 1 ist die oberste Ebene. Wenn ein Absatz mit einer niedrigeren Ebene unter einem Absatz mit einer höheren Ebene liegt,
// Durch das Reduzieren des Absatzes der höheren Ebene wird auch der Absatz der niedrigeren Ebene reduziert.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Zwei Absätze derselben Ebene werden nicht gegenseitig ausgeblendet,
// und die Pfeile reduzieren die Absätze, auf die sie zeigen, nicht.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Der Standardwert „BodyText“ ist der niedrigste, den ein Absatz einer beliebigen Ebene ausblenden kann.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Siehe auch

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


