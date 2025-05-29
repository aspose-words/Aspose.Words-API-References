---
title: Font.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words per .NET
description: Scopri la proprietà Riempimento carattere per migliorare l'aspetto del tuo testo con una formattazione di riempimento personalizzabile, per un aspetto curato e professionale.
type: docs
weight: 130
url: /it/net/aspose.words/font/fill/
---
## Font.Fill property

Ottiene la formattazione di riempimento per il[`Font`](../) .

```csharp
public Fill Fill { get; }
```

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

* class [Fill](../../../aspose.words.drawing/fill/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
