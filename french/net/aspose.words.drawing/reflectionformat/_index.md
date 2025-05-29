---
title: ReflectionFormat Class
linktitle: ReflectionFormat
articleTitle: ReflectionFormat
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.ReflectionFormat pour une mise en forme avancée de la réflexion d'objets. Améliorez la conception de vos documents grâce à une intégration transparente !
type: docs
weight: 1570
url: /fr/net/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class

Représente la mise en forme de réflexion pour un objet.

```csharp
public class ReflectionFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Blur](../../aspose.words.drawing/reflectionformat/blur/) { get; set; } | Obtient ou définit une valeur double qui spécifie le degré d'effet de flou appliqué à l'effet de réflexion en points. La valeur par défaut est 0,0. |
| [Distance](../../aspose.words.drawing/reflectionformat/distance/) { get; set; } | Obtient ou définit une valeur double qui spécifie la quantité de séparation de l'image réfléchie de l'objet en points. La valeur par défaut est 0,0. |
| [Size](../../aspose.words.drawing/reflectionformat/size/) { get; set; } | Obtient ou définit une valeur double entre 0,0 et 1,0 représentant la taille de la réflexion en pourcentage de l'objet réfléchi. La valeur par défaut est 0,0. |
| [Transparency](../../aspose.words.drawing/reflectionformat/transparency/) { get; set; } | Obtient ou définit une valeur double comprise entre 0,0 (opaque) et 1,0 (clair) représentant le degré de transparence pour l'effet de réflexion. La valeur par défaut est 0,0. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Remove](../../aspose.words.drawing/reflectionformat/remove/)() | Supprime`ReflectionFormat` de l'objet parent. |

## Remarques

Utilisez le[`Reflection`](../shapebase/reflection/) propriété pour accéder aux propriétés de réflexion d'un objet. Vous ne créez pas d'instances de la`ReflectionFormat` classe directement.

## Exemples

Montre comment interagir avec l'effet de forme de réflexion.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Reflection.Transparency = 0.37;
shape.Reflection.Size = 0.48;
shape.Reflection.Blur = 17.5;
shape.Reflection.Distance = 9.2;

doc.Save(ArtifactsDir + "Shape.Reflection.docx");

doc = new Document(ArtifactsDir + "Shape.Reflection.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ReflectionFormat reflectionFormat = shape.Reflection;

Assert.AreEqual(0.37d, reflectionFormat.Transparency, 0.01d);
Assert.AreEqual(0.48d, reflectionFormat.Size, 0.01d);
Assert.AreEqual(17.5d, reflectionFormat.Blur, 0.01d);
Assert.AreEqual(9.2d, reflectionFormat.Distance, 0.01d);

reflectionFormat.Remove();

Assert.AreEqual(0, reflectionFormat.Transparency);
Assert.AreEqual(0, reflectionFormat.Size);
Assert.AreEqual(0, reflectionFormat.Blur);
Assert.AreEqual(0, reflectionFormat.Distance);
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
