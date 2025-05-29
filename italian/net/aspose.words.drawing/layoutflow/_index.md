---
title: LayoutFlow Enum
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.LayoutFlow per controllare il layout del testo nelle caselle di testo, migliorando senza sforzo la progettazione e la leggibilità dei tuoi documenti.
type: docs
weight: 1430
url: /it/net/aspose.words.drawing/layoutflow/
---
## LayoutFlow enumeration

Determina il flusso del layout del testo in una casella di testo.

```csharp
public enum LayoutFlow
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Horizontal | `0` | Il testo viene visualizzato orizzontalmente. |
| TopToBottomIdeographic | `1` | Il testo ideografico viene visualizzato verticalmente. |
| BottomToTop | `2` | Il testo viene visualizzato verticalmente. |
| TopToBottom | `3` | Il testo viene visualizzato verticalmente. |
| HorizontalIdeographic | `4` | Il testo ideografico viene visualizzato orizzontalmente. |
| Vertical | `5` | Il testo viene visualizzato verticalmente. |

## Esempi

Mostra come aggiungere testo a una casella di testo e modificarne l'orientamento

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100,
    Height = 100
};
textbox.TextBox.LayoutFlow = LayoutFlow.BottomToTop;

textbox.AppendChild(new Paragraph(doc));
builder.InsertNode(textbox);

builder.MoveTo(textbox.FirstParagraph);
builder.Write("This text is flipped 90 degrees to the left.");

doc.Save(ArtifactsDir + "Drawing.TextBox.docx");
```

### Guarda anche

* property [LayoutFlow](../textbox/layoutflow/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
