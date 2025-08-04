---
title: ListLevel.DeletePictureBullet
linktitle: DeletePictureBullet
articleTitle: DeletePictureBullet
second_title: Aspose.Words for .NET
description: Effortlessly remove picture bullets from your current list level with the ListLevel DeletePictureBullet method. Simplify your document formatting today!
type: docs
weight: 160
url: /net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

Deletes picture bullet for the current list level.

```csharp
public void DeletePictureBullet()
```

## Remarks

Default bullet will be shown after deleting.

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
