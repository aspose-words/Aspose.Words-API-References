---
title: FindReplaceOptions.IgnoreShapes
second_title: Aspose.Words für .NET-API-Referenz
description: FindReplaceOptions eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt ob Formen innerhalb eines Textes ignoriert werden sollen.
type: docs
weight: 110
url: /de/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob Formen innerhalb eines Textes ignoriert werden sollen.

Der Standardwert ist`FALSCH`.

```csharp
public bool IgnoreShapes { get; set; }
```

### Beispiele

Zeigt, wie Formen beim Ersetzen von Text ignoriert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);            
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", new FindReplaceOptions() { IgnoreShapes = true });
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../findreplaceoptions/)
* Montage [Aspose.Words](../../../)


