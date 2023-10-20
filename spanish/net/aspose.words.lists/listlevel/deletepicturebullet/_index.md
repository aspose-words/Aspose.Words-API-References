---
title: ListLevel.DeletePictureBullet
linktitle: DeletePictureBullet
articleTitle: DeletePictureBullet
second_title: Aspose.Words para .NET
description: ListLevel DeletePictureBullet método. Elimina la viñeta de imagen para el nivel de lista actual en C#.
type: docs
weight: 160
url: /es/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

Elimina la viñeta de imagen para el nivel de lista actual.

```csharp
public void DeletePictureBullet()
```

## Observaciones

La viñeta predeterminada se mostrará después de eliminar.

## Ejemplos

Muestra cómo configurar un ícono de imagen personalizado para las etiquetas de elementos de la lista.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Crea una viñeta de imagen para el nivel de lista actual y establece una imagen desde un sistema de archivos local
// como el icono que mostrarán las viñetas de este nivel de lista.
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
