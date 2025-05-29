---
title: BorderCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words per .NET
description: Scopri la proprietà BorderCollection Count per accedere facilmente al numero totale di bordi, migliorando così la flessibilità e l'efficienza della tua progettazione.
type: docs
weight: 30
url: /it/net/aspose.words/bordercollection/count/
---
## BorderCollection.Count property

Ottiene il numero di bordi nella raccolta.

```csharp
public int Count { get; }
```

## Esempi

Mostra come le raccolte di bordi possono condividere elementi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Poiché abbiamo utilizzato la stessa configurazione del bordo durante la creazione
// in questi paragrafi, le raccolte dei bordi condividono gli stessi elementi.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
BorderCollection secondParagraphBorders = builder.CurrentParagraph.ParagraphFormat.Borders;
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsTrue(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());
    Assert.False(firstParagraphBorders[i].IsVisible);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

// Dopo aver modificato lo stile della linea dei bordi solo nel secondo paragrafo,
// le raccolte di bordi non condividono più gli stessi elementi.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    // Modificando l'aspetto di un bordo vuoto, lo si rende visibile.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Guarda anche

* class [BorderCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
