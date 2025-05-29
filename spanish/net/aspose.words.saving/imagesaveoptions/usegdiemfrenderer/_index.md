---
title: ImageSaveOptions.UseGdiEmfRenderer
linktitle: UseGdiEmfRenderer
articleTitle: UseGdiEmfRenderer
second_title: Aspose.Words para .NET
description: Optimice el guardado de EMF con ImageSaveOptions. Controle la configuración del renderizador GDI o Aspose.Words para mejorar la calidad y el rendimiento de la imagen.
type: docs
weight: 190
url: /es/net/aspose.words.saving/imagesaveoptions/usegdiemfrenderer/
---
## ImageSaveOptions.UseGdiEmfRenderer property

Obtiene o establece un valor que determina si se debe utilizar el renderizador de metarchivos GDI+ o Aspose.Words al guardar en EMF.

```csharp
public bool UseGdiEmfRenderer { get; set; }
```

## Observaciones

Si se establece en`verdadero` Se utiliza el renderizador de metarchivos GDI+. Es decir, el contenido se escribe en el objeto graphics de GDI+ y se guarda en un metarchivo.

Si se establece en`FALSO` Se utiliza el renderizador de metarchivos Aspose.Words. Es decir, el contenido se escribe directamente en el formato de metarchivo con Aspose.Words.

Tiene efecto sólo al guardar en EMF.

El guardado en GDI+ sólo funciona en .NET.

El valor predeterminado es`verdadero`.

## Ejemplos

Muestra cómo elegir un renderizador al convertir un documento a .emf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Cuando guardamos el documento como una imagen EMF, podemos pasar un objeto SaveOptions para seleccionar un renderizador para la imagen.
// Si establecemos el indicador "UseGdiEmfRenderer" en "verdadero", Aspose.Words utilizará el renderizador GDI+.
// Si establecemos el indicador "UseGdiEmfRenderer" en "falso", Aspose.Words utilizará su propio renderizador de metarchivos.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Emf);
saveOptions.UseGdiEmfRenderer = useGdiEmfRenderer;

doc.Save(ArtifactsDir + "ImageSaveOptions.Renderer.emf", saveOptions);
```

### Ver también

* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
