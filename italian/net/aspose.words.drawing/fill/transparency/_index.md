---
title: Fill.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words per .NET
description: Regola la trasparenza del riempimento da 0,0 (opaco) a 1,0 (trasparente) per effetti visivi personalizzabili nei tuoi progetti. Migliora l'estetica del tuo progetto oggi stesso!
type: docs
weight: 200
url: /it/net/aspose.words.drawing/fill/transparency/
---
## Fill.Transparency property

Ottiene o imposta il grado di trasparenza del riempimento specificato come valore compreso tra 0,0 (opaco) e 1,0 (trasparente).

```csharp
public double Transparency { get; set; }
```

## Osservazioni

Questa proprietà è l'opposto della proprietà[`Opacity`](../opacity/).

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
