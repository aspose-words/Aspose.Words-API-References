---
title: ShadowFormat.Visible
second_title: Référence de l'API Aspose.Words pour .NET
description: ShadowFormat propriété. Retoursvrai si la mise en forme appliquée à cette instance est visible.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Retours`vrai` si la mise en forme appliquée à cette instance est visible.

```csharp
public bool Visible { get; }
```

### Remarques

Contrairement[`Clear`](../clear/) , assignant`FAUX` to Visible n'efface pas le formatage, il masque uniquement l'effet de forme.

### Exemples

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
* espace de noms [Aspose.Words.Drawing](../../shadowformat/)
* Assemblée [Aspose.Words](../../../)


