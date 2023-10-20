---
title: ShapeBase.MarkupLanguage
linktitle: MarkupLanguage
articleTitle: MarkupLanguage
second_title: Aspose.Words pour .NET
description: ShapeBase MarkupLanguage propriété. Obtient le MarkupLanguage utilisé pour cet objet graphique en C#.
type: docs
weight: 390
url: /fr/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

Obtient le MarkupLanguage utilisé pour cet objet graphique.

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
```

## Exemples

Montre comment vérifier la taille et le langage de balisage d’une forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Voir également

* enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
