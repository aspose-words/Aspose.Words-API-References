---
title: ShadowFormat.Clear
second_title: Aspose.Words für .NET-API-Referenz
description: ShadowFormat methode. Löscht das Schattenformat.
type: docs
weight: 30
url: /de/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Löscht das Schattenformat.

```csharp
public void Clear()
```

### Beispiele

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
* namensraum [Aspose.Words.Drawing](../../shadowformat/)
* Montage [Aspose.Words](../../../)


