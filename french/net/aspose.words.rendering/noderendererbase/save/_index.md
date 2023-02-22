---
title: NodeRendererBase.Save
second_title: Référence de l'API Aspose.Words pour .NET
description: NodeRendererBase méthode. Rend la forme dans une image et lenregistre dans un fichier.
type: docs
weight: 90
url: /fr/net/aspose.words.rendering/noderendererbase/save/
---
## Save(string, ImageSaveOptions) {#save_1}

Rend la forme dans une image et l'enregistre dans un fichier.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Nom du fichier image. Si un fichier portant le nom spécifié existe déjà, le fichier existant est écrasé. |
| saveOptions | ImageSaveOptions | Spécifie les options qui contrôlent le rendu et l'enregistrement de la forme. Peut être nul. |

### Exemples

Montre comment restituer un objet Office Math dans un fichier image dans le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Crée un objet "ImageSaveOptions" à passer à la méthode "Save" du rendu de nœud pour modifier
// comment il rend le nœud OfficeMath dans une image.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Définissez la propriété "Scale" sur 5 pour restituer l'objet à cinq fois sa taille d'origine.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* espace de noms [Aspose.Words.Rendering](../../noderendererbase/)
* Assemblée [Aspose.Words](../../../)

---

## Save(Stream, ImageSaveOptions) {#save}

Rend la forme dans une image et enregistre dans un flux.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux où enregistrer l'image de la forme. |
| saveOptions | ImageSaveOptions | Spécifie les options qui contrôlent le rendu et l'enregistrement de la forme. Peut être nul. S'il est nul, l'image sera enregistrée au format PNG. |

### Exemples

Montre comment utiliser un rendu de forme pour exporter des formes vers des fichiers dans le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Il y a 7 formes dans le document, y compris une forme de groupe avec 2 formes enfants.
// Nous rendrons chaque forme dans un fichier image dans le système de fichiers local
// tout en ignorant les formes de groupe puisqu'elles n'ont pas d'apparence.
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
* espace de noms [Aspose.Words.Rendering](../../noderendererbase/)
* Assemblée [Aspose.Words](../../../)


