---
title: BorderCollection Class
linktitle: BorderCollection
articleTitle: BorderCollection
second_title: Aspose.Words per .NET
description: Aspose.Words.BorderCollection classe. Una raccolta diBorder oggetti in C#.
type: docs
weight: 90
url: /it/net/aspose.words/bordercollection/
---
## BorderCollection class

Una raccolta di[`Border`](../border/) oggetti.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public sealed class BorderCollection : IEnumerable<Border>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bottom](../../aspose.words/bordercollection/bottom/) { get; } | Ottiene il bordo inferiore. |
| [Color](../../aspose.words/bordercollection/color/) { get; set; } | Ottiene o imposta il colore del bordo. |
| [Count](../../aspose.words/bordercollection/count/) { get; } | Ottiene il numero di bordi nella raccolta. |
| [DistanceFromText](../../aspose.words/bordercollection/distancefromtext/) { get; set; } | Ottiene o imposta la distanza del bordo dal testo in punti. |
| [Horizontal](../../aspose.words/bordercollection/horizontal/) { get; } | Ottiene il bordo orizzontale utilizzato tra le celle o i paragrafi conformi. |
| [Item](../../aspose.words/bordercollection/item/) { get; } | Recupera a[`Border`](../border/) oggetto per tipo di bordo. (2 indexers) |
| [Left](../../aspose.words/bordercollection/left/) { get; } | Ottiene il bordo sinistro. |
| [LineStyle](../../aspose.words/bordercollection/linestyle/) { get; set; } | Ottiene o imposta lo stile del bordo. |
| [LineWidth](../../aspose.words/bordercollection/linewidth/) { get; set; } | Ottiene o imposta la larghezza del bordo in punti. |
| [Right](../../aspose.words/bordercollection/right/) { get; } | Ottiene il bordo destro. |
| [Shadow](../../aspose.words/bordercollection/shadow/) { get; set; } | Ottiene o imposta un valore che indica se il bordo ha un'ombra. |
| [Top](../../aspose.words/bordercollection/top/) { get; } | Ottiene il bordo superiore. |
| [Vertical](../../aspose.words/bordercollection/vertical/) { get; } | Ottiene il bordo verticale utilizzato tra le celle. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormatting](../../aspose.words/bordercollection/clearformatting/)() | Rimuove tutti i bordi di un oggetto. |
| [Equals](../../aspose.words/bordercollection/equals/#equals)(*BorderCollection*) | Confronta raccolte di bordi. |
| [GetEnumerator](../../aspose.words/bordercollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti i bordi della raccolta. |

## Osservazioni

Elementi diversi del documento hanno bordi diversi. Ad esempio,[`ParagraphFormat`](../paragraphformat/)ha[`Bottom`](./bottom/) ,[`Left`](./left/) ,[`Right`](./right/) E[`Top`](./top/) bordi. Puoi specificare una formattazione diversa per ciascun bordo in modo indipendente oppure enumerare tutti i bordi e applicare la stessa formattazione.

## Esempi

Mostra come inserire un paragrafo con un bordo superiore.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Imposta ThemeColor solo quando è impostato LineWidth o LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Guarda anche

* class [Border](../border/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
