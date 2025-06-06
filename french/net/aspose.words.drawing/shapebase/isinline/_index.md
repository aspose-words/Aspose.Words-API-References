---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShapeBase IsInline pour vérifier facilement si votre forme s'aligne avec le texte, améliorant ainsi votre conception et l'efficacité de la mise en page.
type: docs
weight: 310
url: /fr/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Un moyen rapide de déterminer si cette forme est positionnée en ligne avec le texte.

```csharp
public bool IsInline { get; }
```

## Remarques

N'a d'effet que sur les formes de niveau supérieur.

## Exemples

Montre comment déterminer si une forme est en ligne ou flottante.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux types d'emballage que les formes peuvent avoir.
// 1 - En ligne :
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Une forme en ligne se trouve à l'intérieur d'un paragraphe parmi d'autres éléments de paragraphe, tels que des séquences de texte.
// Dans Microsoft Word, nous pouvons cliquer et faire glisser la forme vers n’importe quel paragraphe comme s’il s’agissait d’un caractère.
// Si la forme est grande, cela affectera l'espacement vertical des paragraphes.
// Nous ne pouvons pas déplacer cette forme vers un endroit sans paragraphe.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Flottant :
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Une forme flottante appartient au paragraphe dans lequel nous l'insérons,
// que nous pouvons déterminer par un symbole d'ancrage qui apparaît lorsque nous cliquons sur la forme.
// Si la forme n'a pas de symbole d'ancrage visible à sa gauche,
// nous devrons activer les ancres visibles via "Options" -> "Affichage" -> "Ancres d'objet".
// Dans Microsoft Word, nous pouvons cliquer avec le bouton gauche de la souris et faire glisser cette forme librement vers n'importe quel emplacement.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
