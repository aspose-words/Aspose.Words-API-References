---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
second_title: Aspose.Words for .NET API Reference
description: ListLevel CreatePictureBullet method. Creates picture bullet shape for the current list level in C#.
type: docs
weight: 150
url: /net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

Creates picture bullet shape for the current list level.

```csharp
public void CreatePictureBullet()
```

## Remarks

Please note, [`NumberStyle`](../numberstyle/) will be set to Bullet and [`NumberFormat`](../numberformat/) to "\xF0B7" to properly display picture bullet. Red cross image will be set as picture bullet image upon creating. To change it please use [`ImageData`](../imagedata/).

## Examples

Shows how to set a custom image icon for list item labels.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Create a picture bullet for the current list level, and set an image from a local file system
// as the icon that the bullets for this list level will display.
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

### See Also

* class [ListLevel](../)
* namespace [Aspose.Words.Lists](../../listlevel/)
* assembly [Aspose.Words](../../../)
