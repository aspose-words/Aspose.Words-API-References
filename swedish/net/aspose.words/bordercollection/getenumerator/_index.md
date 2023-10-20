---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: BorderCollection GetEnumerator metod. Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla gränser i samlingen i C#.
type: docs
weight: 160
url: /sv/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla gränser i samlingen.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## Exempel

Visar hur man itererar över och redigerar alla kanter i ett objekt i styckeformat.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Konfigurera byggarens styckeformatinställningar för att skapa en grön vågkant på alla sidor.
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

// Infoga ett stycke. Våra kantinställningar kommer att avgöra utseendet på dess kant.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### Se även

* class [Border](../../border/)
* class [BorderCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
