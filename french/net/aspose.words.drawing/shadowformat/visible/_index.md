---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShadowFormat Visible. Vérifiez facilement si votre mise en forme est visible, améliorant ainsi l'apparence et la clarté de votre document.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Retours`vrai` si la mise en forme appliquée à cette instance est visible.

```csharp
public bool Visible { get; }
```

## Remarques

Contrairement à[`Clear`](../clear/) , attribuant`FAUX`Visible n'efface pas la mise en forme, il masque uniquement l'effet de forme.

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
