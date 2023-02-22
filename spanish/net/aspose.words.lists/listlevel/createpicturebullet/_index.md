---
title: ListLevel.CreatePictureBullet
second_title: Referencia de API de Aspose.Words para .NET
description: ListLevel método. Crea una forma de viñeta de imagen para el nivel de lista actual.
type: docs
weight: 150
url: /es/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

Crea una forma de viñeta de imagen para el nivel de lista actual.

```csharp
public void CreatePictureBullet()
```

### Observaciones

Tenga en cuenta que NumberStyle se establecerá en Bullet y NumberFormat en "\xF0B7" para mostrar correctamente la imagen de viñeta. La imagen de la cruz roja se establecerá como imagen de viñeta al crearla. Para cambiarlo, utilice[`ImageData`](../imagedata/).

### Ejemplos

Muestra cómo configurar un icono de imagen personalizado para las etiquetas de los elementos de la lista.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Crear una viñeta de imagen para el nivel de lista actual y establecer una imagen desde un sistema de archivos local
// como el icono que mostrarán las viñetas para este nivel de lista.
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
* espacio de nombres [Aspose.Words.Lists](../../listlevel/)
* asamblea [Aspose.Words](../../../)


