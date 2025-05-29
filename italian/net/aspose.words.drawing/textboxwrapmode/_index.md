---
title: TextBoxWrapMode Enum
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words per .NET
description: Scopri l'enumerazione Aspose.Words.Drawing.TextBoxWrapMode per controllare l'avvolgimento del testo nelle forme, migliorando i layout dei documenti e la flessibilità di progettazione.
type: docs
weight: 1750
url: /it/net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

Specifica come il testo viene disposto all'interno di una forma.

```csharp
public enum TextBoxWrapMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Square | `0` | Il testo si inserisce all'interno di una forma. |
| None | `2` | Il testo non si adatta all'interno di una forma. |

## Esempi

Mostra come impostare una modalità di avvolgimento per il contenuto di una casella di testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Imposta la proprietà "TextBoxWrapMode" su "TextBoxWrapMode.None" per aumentare la larghezza della casella di testo
// per contenere il testo, se sufficientemente grande.
// Imposta la proprietà "TextBoxWrapMode" su "TextBoxWrapMode.Square" per
// racchiude tutto il testo all'interno della casella di testo, mantenendone le dimensioni.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
