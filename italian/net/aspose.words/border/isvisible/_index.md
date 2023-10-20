---
title: Border.IsVisible
linktitle: IsVisible
articleTitle: IsVisible
second_title: Aspose.Words per .NET
description: Border IsVisible proprietà. RestituisceVERO se laLineStyle non èNone  in C#.
type: docs
weight: 30
url: /it/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Restituisce`VERO` se la[`LineStyle`](../linestyle/) non èNone .

```csharp
public bool IsVisible { get; }
```

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
