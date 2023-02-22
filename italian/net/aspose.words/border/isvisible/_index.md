---
title: Border.IsVisible
second_title: Aspose.Words per .NET API Reference
description: Border proprietà. Restituisce true se LineStyle non è LineStyle.None.
type: docs
weight: 30
url: /it/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Restituisce true se LineStyle non è LineStyle.None.

```csharp
public bool IsVisible { get; }
```

### Esempi

Mostra come rimuovere i bordi da un paragrafo.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Ogni paragrafo ha un insieme individuale di bordi.
// Possiamo accedere alle impostazioni per l'aspetto di questi bordi tramite l'oggetto formato paragrafo.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

// Possiamo rimuovere un bordo in una volta eseguendo il metodo ClearFormatting. 
// L'esecuzione di questo metodo su ogni bordo di un paragrafo rimuoverà tutti i suoi bordi.
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
* spazio dei nomi [Aspose.Words](../../border/)
* assemblea [Aspose.Words](../../../)


