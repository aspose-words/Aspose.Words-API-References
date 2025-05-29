---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words per .NET
description: Scopri la proprietà Colore riempimento per personalizzare facilmente il colore di primo piano del tuo progetto con un oggetto Colore, migliorando così l'aspetto visivo del tuo progetto.
type: docs
weight: 50
url: /it/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

Ottiene o imposta un oggetto Color che rappresenta il colore di primo piano per il riempimento.

```csharp
public Color Color { get; set; }
```

## Osservazioni

Questa proprietà preserva la componente alfa dell'Color , a differenza del[`ForeColor`](../forecolor/) proprietà, che lo reimposta su un colore completamente opaco.

## Esempi

Mostra come riconvertire uno qualsiasi dei riempimenti in riempimento uniforme.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Ottieni l'oggetto Fill per il font della prima esecuzione.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Controlla le proprietà di riempimento del font.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Cambia il tipo di riempimento in Solido con colore verde uniforme.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Guarda anche

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
