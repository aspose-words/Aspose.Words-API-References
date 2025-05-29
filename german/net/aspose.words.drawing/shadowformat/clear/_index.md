---
title: ShadowFormat.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words für .NET
description: Setzen Sie Ihr Schattenformat mühelos mit der ShadowFormat Clear-Methode zurück. Verbessern Sie Ihr Design noch heute mit einem sauberen Blatt!
type: docs
weight: 40
url: /de/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Löscht das Schattenformat.

```csharp
public void Clear()
```

## Beispiele

Zeigt, wie mit einer Schattenformatierung für die Form gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)
    shape.ShadowFormat.Clear();
```

### Siehe auch

* class [ShadowFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
