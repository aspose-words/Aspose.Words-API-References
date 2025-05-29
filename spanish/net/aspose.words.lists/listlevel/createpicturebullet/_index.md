---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
articleTitle: CreatePictureBullet
second_title: Aspose.Words para .NET
description: Descubra el método ListLevel CreatePictureBullet para mejorar sin esfuerzo sus listas con viñetas de imágenes personalizadas, agregando atractivo visual y claridad.
type: docs
weight: 150
url: /es/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

Crea una forma de viñeta de imagen para el nivel de lista actual.

```csharp
public void CreatePictureBullet()
```

## Observaciones

Tenga en cuenta,[`NumberStyle`](../numberstyle/) se establecerá enBullet y [`NumberFormat`](../numberformat/) a "\xF0B7" para mostrar correctamente la viñeta de imagen. La imagen de la cruz roja se establecerá como imagen de viñeta de imagen al crearla. Para cambiarla, utilice[`ImageData`](../imagedata/).

## Ejemplos

Muestra cómo establecer un ícono de imagen personalizado para las etiquetas de elementos de la lista.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Crea una viñeta de imagen para el nivel de lista actual y establece una imagen desde un sistema de archivos local
// como el ícono que mostrarán las viñetas para este nivel de lista.
list.ListLevels[0].CreatePictureBullet();
list.ListLevels[0].ImageData.SetImage(ImageDir + "Logo icon.ico");

Assert.IsTrue(list.ListLevels[0].ImageData.HasImage);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("Hello world!");
builder.Write("Hello again!");

doc.Save(ArtifactsDir + "Lists.CreatePictureBullet.docx");

list.ListLevels[0].DeletePictureBullet();

Assert.IsNull(list.ListLevels[0].ImageData);
```

### Ver también

* class [ListLevel](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
