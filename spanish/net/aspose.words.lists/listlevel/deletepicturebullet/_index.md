---
title: ListLevel.DeletePictureBullet
second_title: Referencia de API de Aspose.Words para .NET
description: ListLevel método. Elimina la viñeta de imagen para el nivel de lista actual.
type: docs
weight: 160
url: /es/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

Elimina la viñeta de imagen para el nivel de lista actual.

```csharp
public void DeletePictureBullet()
```

### Observaciones

La viñeta predeterminada se mostrará después de eliminar.

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


