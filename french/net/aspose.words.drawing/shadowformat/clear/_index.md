---
title: ShadowFormat.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words pour .NET
description: Réinitialisez facilement le format de votre ombre grâce à la méthode ShadowFormat Clear. Améliorez votre design dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Efface le format d'ombre.

```csharp
public void Clear()
```

## Exemples

Montre comment travailler avec une mise en forme d'ombre pour la forme.

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
