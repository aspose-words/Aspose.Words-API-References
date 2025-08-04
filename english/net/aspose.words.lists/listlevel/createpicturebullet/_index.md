---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
articleTitle: CreatePictureBullet
second_title: Aspose.Words for .NET
description: Discover the ListLevel CreatePictureBullet method to effortlessly enhance your lists with custom picture bullets, adding visual appeal and clarity.
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

List docList = doc.Lists.Add(ListTemplate.BulletCircle);

// Create a picture bullet for the current list level, and set an image from a local file system
// as the icon that the bullets for this list level will display.
docList.ListLevels[0].CreatePictureBullet();
docList.ListLevels[0].ImageData.SetImage(ImageDir + "Logo icon.ico");

Assert.That(docList.ListLevels[0].ImageData.HasImage, Is.True);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = docList;
builder.Writeln("Hello world!");
builder.Write("Hello again!");

doc.Save(ArtifactsDir + "Lists.CreatePictureBullet.docx");

docList.ListLevels[0].DeletePictureBullet();

Assert.That(docList.ListLevels[0].ImageData, Is.Null);
```

### See Also

* class [ListLevel](../)
* namespace [Aspose.Words.Lists](../../../aspose.words.lists/)
* assembly [Aspose.Words](../../../)
