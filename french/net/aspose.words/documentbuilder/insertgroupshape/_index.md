---
title: DocumentBuilder.InsertGroupShape
linktitle: InsertGroupShape
articleTitle: InsertGroupShape
second_title: Aspose.Words pour .NET
description: Regroupez facilement des formes grâce à la méthode InsertGroupShape de DocumentBuilder. Créez des designs organisés en insérant facilement de nouveaux nœuds GroupShape.
type: docs
weight: 360
url: /fr/net/aspose.words/documentbuilder/insertgroupshape/
---
## InsertGroupShape(*params ShapeBase[]*) {#insertgroupshape}

Regroupe les formes passées en paramètre dans un nouveau nœud GroupShape qui est inséré dans la position actuelle.

```csharp
public GroupShape InsertGroupShape(params ShapeBase[] shapes)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| shapes | ShapeBase[] | La liste des formes à regrouper. |

## Remarques

La position et la dimension du nouveau GroupShape seront calculées automatiquement.

Les formes VML et DML ne peuvent pas être regroupées.

## Exemples

Montre comment combiner la forme du groupe avec la forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Combinez les formes dans un nœud GroupShape qui est inséré dans la position spécifiée.
GroupShape groupShape1 = builder.InsertGroupShape(shape1, shape2);

// Combinez les nœuds Shape et GroupShape.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(groupShape1, shape3);

doc.Save(ArtifactsDir + "Shape.CombineGroupShape.docx");
```

Montre comment insérer une forme de groupe DML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Dimensions du nouveau nœud GroupShape.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Insérer un nœud GroupShape pour la taille spécifiée qui est inséré dans la position spécifiée.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Insérer un nœud GroupShape dont la position et la dimension seront calculées automatiquement.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Voir également

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertGroupShape(*double, double, double, double, params ShapeBase[]*) {#insertgroupshape_1}

Regroupe les formes passées en paramètre dans un nouveau nœud GroupShape de la taille spécifiée qui est inséré dans la position spécifiée.

```csharp
public GroupShape InsertGroupShape(double left, double top, double width, double height, 
    params ShapeBase[] shapes)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| left | Double | Distance en points de l'origine au côté gauche de la forme du groupe. |
| top | Double | Distance en points de l'origine au côté supérieur de la forme du groupe. |
| width | Double | Largeur du groupe en points. Une valeur négative n'est pas autorisée. |
| height | Double | Hauteur du groupe en points. Une valeur négative n'est pas autorisée. |
| shapes | ShapeBase[] | La liste des formes à regrouper. |

## Remarques

Les formes VML et DML ne peuvent pas être regroupées.

## Exemples

Montre comment insérer une forme de groupe DML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape1 = builder.InsertShape(ShapeType.Rectangle, 200, 250);
shape1.Left = 20;
shape1.Top = 20;
shape1.Stroke.Color = Color.Red;

Shape shape2 = builder.InsertShape(ShapeType.Ellipse, 150, 200);
shape2.Left = 40;
shape2.Top = 50;
shape2.Stroke.Color = Color.Green;

// Dimensions du nouveau nœud GroupShape.
double left = 10;
double top = 10;
double width = 200;
double height = 300;
// Insérer un nœud GroupShape pour la taille spécifiée qui est inséré dans la position spécifiée.
GroupShape groupShape1 = builder.InsertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

// Insérer un nœud GroupShape dont la position et la dimension seront calculées automatiquement.
Shape shape3 = (Shape)shape1.Clone(true);
GroupShape groupShape2 = builder.InsertGroupShape(shape3);

doc.Save(ArtifactsDir + "Shape.InsertGroupShape.docx");
```

### Voir également

* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
