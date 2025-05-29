---
title: Border.IsVisible
linktitle: IsVisible
articleTitle: IsVisible
second_title: Aspose.Words per .NET
description: Scopri come la proprietà Border IsVisible migliora il tuo design restituendo true quando viene applicato LineStyle. Ottimizza la tua interfaccia utente con questa funzionalità chiave!
type: docs
weight: 30
url: /it/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Restituisce`VERO` se il[`LineStyle`](../linestyle/) non èNone .

```csharp
public bool IsVisible { get; }
```

## Esempi

Mostra come rimuovere i bordi da un paragrafo.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Ogni paragrafo ha un set di bordi individuale.
// Possiamo accedere alle impostazioni per l'aspetto di questi bordi tramite l'oggetto formato paragrafo.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 // Possiamo rimuovere un bordo in una volta eseguendo il metodo ClearFormatting.
// Eseguendo questo metodo su ogni bordo di un paragrafo verranno rimossi tutti i suoi bordi.
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
