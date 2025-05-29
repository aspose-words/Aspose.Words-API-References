---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
articleTitle: CreatePictureBullet
second_title: Aspose.Words för .NET
description: Upptäck ListLevel CreatePictureBullet-metoden för att enkelt förbättra dina listor med anpassade bildpunkter, vilket ger visuell attraktionskraft och tydlighet.
type: docs
weight: 150
url: /sv/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

Skapar en punktformad bild för den aktuella listnivån.

```csharp
public void CreatePictureBullet()
```

## Anmärkningar

Observera,[`NumberStyle`](../numberstyle/) kommer att ställas in påBullet och [`NumberFormat`](../numberformat/) till "\xF0B7" för att visa bildpunkten korrekt. Röda korsbilden kommer att ställas in som bildpunktbild när den skapas. För att ändra den, använd[`ImageData`](../imagedata/).

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
