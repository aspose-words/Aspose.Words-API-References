---
title: NodeRendererBase.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words para .NET
description: NodeRendererBase Save método. Representa la forma en una imagen y la guarda en un archivo en C#.
type: docs
weight: 90
url: /es/net/aspose.words.rendering/noderendererbase/save/
---
## Save(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save_1}

Representa la forma en una imagen y la guarda en un archivo.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El nombre del archivo de imagen. Si ya existe un archivo con el nombre especificado, se sobrescribe el archivo existente. |
| saveOptions | ImageSaveOptions | Especifica las opciones que controlan cómo se representa y guarda la forma. Puede ser`nulo`. |

## Ejemplos

Muestra cómo representar un objeto de Office Math en un archivo de imagen en el sistema de archivos local.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Crea un objeto "ImageSaveOptions" para pasarlo al método "Guardar" del renderizador de nodos para modificarlo
// cómo representa el nodo OfficeMath en una imagen.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Establece la propiedad "Escala" en 5 para representar el objeto cinco veces su tamaño original.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* espacio de nombres [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../../)

---

## Save(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save}

Representa la forma en una imagen y la guarda en una secuencia.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | La secuencia donde guardar la imagen de la forma. |
| saveOptions | ImageSaveOptions | Especifica las opciones que controlan cómo se representa y guarda la forma. Puede ser`nulo` . Si esto es`nulo`, la imagen se guardará en formato PNG. |

## Ejemplos

Muestra cómo utilizar un procesador de formas para exportar formas a archivos en el sistema de archivos local.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Hay 7 formas en el documento, incluida una forma de grupo con 2 formas secundarias.
// Representaremos cada forma en un archivo de imagen en el sistema de archivos local
// ignorando las formas del grupo ya que no tienen apariencia.
// Esto producirá 6 archivos de imagen.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* espacio de nombres [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../../)
