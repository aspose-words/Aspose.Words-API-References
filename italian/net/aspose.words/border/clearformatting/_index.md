---
title: Border.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words per .NET
description: Border ClearFormatting metodo. Ripristina le proprietà del bordo ai valori predefiniti in C#.
type: docs
weight: 90
url: /it/net/aspose.words/border/clearformatting/
---
## Border.ClearFormatting method

Ripristina le proprietà del bordo ai valori predefiniti.

```csharp
public void ClearFormatting()
```

## Osservazioni

Quando le proprietà del bordo vengono ripristinate ai valori predefiniti, il bordo è invisibile.

## Esempi

Mostra come rimuovere i bordi da un paragrafo.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Ogni paragrafo ha un insieme di bordi individuale.
// Possiamo accedere alle impostazioni per l'aspetto di questi bordi tramite l'oggetto formato paragrafo.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 // Possiamo rimuovere immediatamente un bordo eseguendo il metodo ClearFormatting.
// L'esecuzione di questo metodo su ogni bordo di un paragrafo ne rimuoverà tutti i bordi.
foreach (Border border in borders)
    border.ClearFormatting();

Assert.AreEqual(Color.Empty.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(0.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.None, borders[0].LineStyle);
Assert.IsFalse(borders[0].IsVisible);

doc.Save(ArtifactsDir + "Border.ClearFormatting.docx");
```

### Guarda anche

* class [Border](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
