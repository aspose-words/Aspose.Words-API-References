---
title: BorderCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Scopri la proprietà BorderCollection Item per accedere facilmente agli oggetti Border per tipo. Semplifica il tuo design con una gestione efficiente dei bordi!
type: docs
weight: 60
url: /it/net/aspose.words/bordercollection/item/
---
## BorderCollection indexer (1 of 2)

Recupera un[`Border`](../../border/) oggetto per tipo di bordo.

```csharp
public Border this[BorderType borderType] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| borderType | UN[`BorderType`](../../bordertype/) value che specifica il tipo di bordo da recuperare. |

## Osservazioni

Si noti che non tutti i bordi sono presenti per i diversi elementi del documento. Questo metodo genera un'eccezione se si richiede un bordo non applicabile all'oggetto corrente.

## Esempi

Mostra come decorare il testo con bordi e ombreggiature.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### Guarda anche

* class [Border](../../border/)
* enum [BorderType](../../bordertype/)
* class [BorderCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## BorderCollection indexer (2 of 2)

Recupera un[`Border`](../../border/) oggetto per indice.

```csharp
public Border this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Indice a partire da zero del confine da recuperare. |

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

* class [Border](../../border/)
* class [BorderCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
