---
title: NodeRendererBase.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Save de NodeRendererBase. Générez facilement des formes sous forme d'images et enregistrez-les dans des fichiers pour une intégration fluide et une productivité accrue.
type: docs
weight: 90
url: /fr/net/aspose.words.rendering/noderendererbase/save/
---
## Save(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save_2}

Rend la forme dans une image et l'enregistre dans un fichier.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom du fichier image. Si un fichier portant le nom spécifié existe déjà, il est écrasé. |
| saveOptions | ImageSaveOptions | Spécifie les options qui contrôlent le rendu et l'enregistrement de la forme. Peut être`nul`. |

## Exemples

Montre comment restituer un objet Office Math dans un fichier image dans le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Créez un objet « ImageSaveOptions » à transmettre à la méthode « Save » du moteur de rendu du nœud pour modifier
// comment il rend le nœud OfficeMath dans une image.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Définissez la propriété « Scale » sur 5 pour rendre l'objet à cinq fois sa taille d'origine.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)

---

## Save(*string, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_3}

Rend la forme dans une image SVG et l'enregistre dans un fichier.

```csharp
public void Save(string fileName, SvgSaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom du fichier image. Si un fichier portant le nom spécifié existe déjà, il est écrasé. |
| saveOptions | SvgSaveOptions | Spécifie les options qui contrôlent le rendu et l'enregistrement de la forme. Peut être`nul`. |

## Exemples

Montre comment transmettre les options de sauvegarde lors du rendu des mathématiques de bureau.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Voir également

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)

---

## Save(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save}

Rend la forme dans une image et l'enregistre dans un flux.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux où enregistrer l'image de la forme. |
| saveOptions | ImageSaveOptions | Spécifie les options qui contrôlent le rendu et l'enregistrement de la forme. Peut être`nul` . Si c'est le cas`nul`l'image sera enregistrée au format PNG. |

## Exemples

Montre comment utiliser un moteur de rendu de formes pour exporter des formes vers des fichiers dans le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Il y a 7 formes dans le document, dont une forme de groupe avec 2 formes enfants.
// Nous allons rendre chaque forme dans un fichier image dans le système de fichiers local
// tout en ignorant les formes de groupe car elles n'ont aucune apparence.
// Cela produira 6 fichiers image.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)

---

## Save(*Stream, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_1}

Rend la forme dans une image SVG et l'enregistre dans un flux.

```csharp
public void Save(Stream stream, SvgSaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux où enregistrer l'image SVG de la forme. |
| saveOptions | SvgSaveOptions | Spécifie les options qui contrôlent le rendu et l'enregistrement de la forme. Peut être`nul` . Si c'est le cas`nul`, l'image sera enregistrée avec les options par défaut. |

## Exemples

Montre comment transmettre les options de sauvegarde lors du rendu des mathématiques de bureau.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Voir également

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)
