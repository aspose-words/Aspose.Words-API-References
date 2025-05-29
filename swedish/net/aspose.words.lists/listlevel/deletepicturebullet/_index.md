---
title: ListLevel.DeletePictureBullet
linktitle: DeletePictureBullet
articleTitle: DeletePictureBullet
second_title: Aspose.Words för .NET
description: Ta enkelt bort bildpunkter från din nuvarande listnivå med ListLevel DeletePictureBullet-metoden. Förenkla din dokumentformatering idag!
type: docs
weight: 160
url: /sv/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

Tar bort bildpunkten för den aktuella listnivån.

```csharp
public void DeletePictureBullet()
```

## Anmärkningar

Standardpunkten visas efter borttagning.

## Exempel

Visar hur man ställer in en anpassad bildikon för listobjektsetiketter.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Skapa en bildpunkt för den aktuella listnivån och ange en bild från ett lokalt filsystem
// som ikonen som punkterna för den här listnivån kommer att visa.
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

### Se även

* class [ListLevel](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
