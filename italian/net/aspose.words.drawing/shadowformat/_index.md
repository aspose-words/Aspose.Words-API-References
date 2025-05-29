---
title: ShadowFormat Class
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Drawing.ShadowFormat per effetti ombra migliorati sugli oggetti. Migliora il design dei tuoi documenti con opzioni di formattazione delle ombre personalizzabili.
type: docs
weight: 1620
url: /it/net/aspose.words.drawing/shadowformat/
---
## ShadowFormat class

Rappresenta la formattazione ombra per un oggetto.

Per saperne di più, visita il[Lavorare con gli elementi grafici](https://docs.aspose.com/words/net/working-with-graphic-elements/) articolo di documentazione.

```csharp
public class ShadowFormat
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Color](../../aspose.words.drawing/shadowformat/color/) { get; } | Ottiene unColor oggetto che rappresenta il colore dell'ombra. Il valore predefinito èBlack . |
| [Type](../../aspose.words.drawing/shadowformat/type/) { get; set; } | Ottiene o imposta il valore specificato[`ShadowType`](../shadowtype/) per ShadowFormat. |
| [Visible](../../aspose.words.drawing/shadowformat/visible/) { get; } | Restituisce`VERO` se la formattazione applicata a questa istanza è visibile. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clear](../../aspose.words.drawing/shadowformat/clear/)() | Cancella il formato ombra. |

## Esempi

Mostra come ottenere il colore dell'ombra.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
