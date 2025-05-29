---
title: BorderCollection.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words per .NET
description: Scopri il metodo BorderCollection Equals per confrontare in modo efficiente le collezioni di bordi e migliorare la tua produttività di programmazione. Ottimizza i tuoi progetti oggi stesso!
type: docs
weight: 150
url: /it/net/aspose.words/bordercollection/equals/
---
## BorderCollection.Equals method

Confronta raccolte di bordi.

```csharp
public bool Equals(BorderCollection brColl)
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
