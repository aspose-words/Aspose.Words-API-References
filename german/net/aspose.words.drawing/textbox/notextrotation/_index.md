---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: Aspose.Words für .NET
description: Steuern Sie die Textdrehung in Ihrer TextBox mit der Eigenschaft „NoTextRotation“. Sorgen Sie für klaren, lesbaren Text, auch bei gedrehten Formen. Verbessern Sie Ihr Design!
type: docs
weight: 80
url: /de/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, dass der Text des Textfelds nicht gedreht werden soll, wenn die Form gedreht wird.

```csharp
public bool NoTextRotation { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH`

## Beispiele

Zeigt, wie die Textdrehung deaktiviert wird, wenn die Form gedreht wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### Siehe auch

* class [TextBox](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
