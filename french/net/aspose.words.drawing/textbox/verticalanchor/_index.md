---
title: TextBox.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété TextBox VerticalAnchor améliore l'alignement du texte dans les formes pour une conception et une lisibilité améliorées dans vos projets.
type: docs
weight: 120
url: /fr/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

Spécifie l'alignement vertical du texte dans une forme.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

## Remarques

La valeur par défaut estTop.

## Exemples

Montre comment aligner verticalement le contenu textuel d'une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Définissez la propriété « VerticalAnchor » sur « TextBoxAnchor.Top » pour
// alignez le texte dans cette zone de texte avec le côté supérieur de la forme.
// Définissez la propriété « VerticalAnchor » sur « TextBoxAnchor.Middle » pour
// alignez le texte de cette zone de texte au centre de la forme.
// Définissez la propriété « VerticalAnchor » sur « TextBoxAnchor.Bottom » pour
// alignez le texte de cette zone de texte sur le bas de la forme.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// L'alignement vertical du texte à l'intérieur des zones de texte est disponible à partir de Microsoft Word 2007.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Voir également

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
