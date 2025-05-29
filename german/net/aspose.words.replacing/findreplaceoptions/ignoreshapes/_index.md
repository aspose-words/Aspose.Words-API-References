---
title: FindReplaceOptions.IgnoreShapes
linktitle: IgnoreShapes
articleTitle: IgnoreShapes
second_title: Aspose.Words für .NET
description: Entdecken Sie die IgnoreShapes-Eigenschaft von FindReplaceOptions. Steuern Sie die Einbindung von Formen in die Textverarbeitung mit dieser wichtigen booleschen Einstellung für verbesserte Genauigkeit.
type: docs
weight: 110
url: /de/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Formen innerhalb eines Textes ignoriert werden sollen.

Der Standardwert ist`FALSCH`.

```csharp
public bool IgnoreShapes { get; set; }
```

## Beispiele

Zeigt, wie Formen beim Ersetzen von Text ignoriert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

FindReplaceOptions findReplaceOptions = new FindReplaceOptions() { IgnoreShapes = true };
builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
