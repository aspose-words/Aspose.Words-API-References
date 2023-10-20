---
title: ShadowFormat.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words pour .NET
description: ShadowFormat Clear méthode. Efface le format dombre en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Efface le format d'ombre.

```csharp
public void Clear()
```

## Exemples

Montre comment utiliser un formatage d’ombre pour la forme.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)                
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)            
    shape.ShadowFormat.Clear();
```

### Voir également

* class [ShadowFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
