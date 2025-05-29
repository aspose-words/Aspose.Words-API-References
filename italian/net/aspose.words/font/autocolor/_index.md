---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font AutoColor, ottieni il colore del testo corrente (nero o bianco) per regolazioni automatiche. Ottimizza il tuo design senza sforzo!
type: docs
weight: 20
url: /it/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

Restituisce il colore calcolato attuale del testo (nero o bianco) da utilizzare per 'colore automatico'. Se il colore non è 'automatico', restituisce[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

## Osservazioni

Quando il testo ha un "colore automatico", il colore effettivo del testo viene calcolato automaticamente in modo che sia leggibile rispetto al colore di sfondo. Quando si cambia il colore di sfondo, il colore del testo passerà automaticamente al nero o al bianco in MS Word per massimizzare la leggibilità.

## Esempi

Mostra come migliorare la leggibilità selezionando automaticamente il colore del testo in base alla luminosità dello sfondo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se l'oggetto Font di un'esecuzione non specifica il colore del testo, verrà automaticamente
// seleziona nero o bianco a seconda del colore di sfondo.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// Il colore predefinito per il testo è il nero. Se il colore dello sfondo è scuro, il testo nero sarà difficile da vedere.
// Per risolvere questo problema, la proprietà AutoColor visualizzerà questo testo in bianco.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// Se cambiamo lo sfondo con un colore chiaro, il nero sarà più
// colore del testo più adatto del bianco, in modo che il colore automatico lo visualizzi in nero.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
