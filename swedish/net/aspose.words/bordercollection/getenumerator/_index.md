---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: Upptäck BorderCollection GetEnumerator-metoden för att enkelt iterera genom alla gränser, vilket förbättrar din kodningseffektivitet och samlingshantering.
type: docs
weight: 160
url: /sv/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

Returnerar ett uppräknarobjekt som kan användas för att iterera över alla gränser i samlingen.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## Exempel

Visar hur man itererar över och redigerar alla kantlinjer i ett styckeformatobjekt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Konfigurera inställningarna för styckeformat i verktyget för att skapa en grön vågkant på alla sidor.
BorderCollection borders = builder.ParagraphFormat.Borders;

using (IEnumerator<Border> enumerator = borders.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Border border = enumerator.Current;
        border.Color = Color.Green;
        border.LineStyle = LineStyle.Wave;
        border.LineWidth = 3;
    }
}

// Infoga ett stycke. Våra kantinställningar avgör hur kanten ska se ut.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### Se även

* class [Border](../../border/)
* class [BorderCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
