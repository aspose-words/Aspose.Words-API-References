---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words per .NET
description: Fill Solid metodo. Imposta il riempimento su un colore uniforme in C#.
type: docs
weight: 250
url: /it/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

Imposta il riempimento su un colore uniforme.

```csharp
public void Solid()
```

## Osservazioni

Utilizza questo metodo per riconvertire qualsiasi riempimento in riempimento solido.

### Guarda anche

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

Imposta il riempimento su un colore uniforme specificato.

```csharp
public void Solid(Color color)
```

## Osservazioni

Utilizza questo metodo per riconvertire qualsiasi riempimento in riempimento solido.

## Esempi

Mostra come riconvertire uno qualsiasi dei riempimenti in riempimento solido.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Ottieni l'oggetto Fill per il Font della prima esecuzione.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Controlla le proprietà di riempimento del carattere.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Cambia il tipo di riempimento in Solido con colore verde uniforme.
fill.Solid(Color.Green);
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
