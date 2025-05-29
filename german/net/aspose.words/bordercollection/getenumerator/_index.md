---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words für .NET
description: Entdecken Sie die BorderCollection GetEnumerator-Methode, um einfach durch alle Grenzen zu iterieren und so Ihre Codierungseffizienz und Sammlungsverwaltung zu verbessern.
type: docs
weight: 160
url: /de/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

Gibt ein Enumeratorobjekt zurück, mit dem alle Grenzen in der Sammlung durchlaufen werden können.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## Beispiele

Zeigt, wie alle Rahmen in einem Absatzformatobjekt durchlaufen und bearbeitet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Konfigurieren Sie die Absatzformateinstellungen des Builders, um auf allen Seiten einen grünen Wellenrand zu erstellen.
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

// Fügen Sie einen Absatz ein. Unsere Rahmeneinstellungen bestimmen das Erscheinungsbild des Rahmens.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### Siehe auch

* class [Border](../../border/)
* class [BorderCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
