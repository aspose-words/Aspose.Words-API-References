---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words per .NET
description: Scopri il metodo GetEnumerator di BorderCollection per scorrere facilmente tutti i bordi, migliorando l'efficienza della codifica e la gestione delle raccolte.
type: docs
weight: 160
url: /it/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti i bordi della raccolta.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## Esempi

Mostra come scorrere e modificare tutti i bordi in un oggetto formato paragrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configura le impostazioni del formato paragrafo del builder per creare un bordo ondulato verde su tutti i lati.
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

// Inserisci un paragrafo. Le nostre impostazioni dei bordi determineranno l'aspetto del bordo.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### Guarda anche

* class [Border](../../border/)
* class [BorderCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
