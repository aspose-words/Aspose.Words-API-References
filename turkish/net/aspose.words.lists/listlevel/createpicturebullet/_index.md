---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
articleTitle: CreatePictureBullet
second_title: .NET için Aspose.Words
description: Listelerinizi özel resimli maddelerle zahmetsizce zenginleştirmek, görsel çekicilik ve netlik katmak için ListLevel CreatePictureBullet yöntemini keşfedin.
type: docs
weight: 150
url: /tr/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

Mevcut liste düzeyi için resim madde işareti şekli oluşturur.

```csharp
public void CreatePictureBullet()
```

## Notlar

Lütfen aklınızda bulundurun,[`NumberStyle`](../numberstyle/) ayarlanacakBullet ve [`NumberFormat`](../numberformat/) Resim madde işaretini düzgün bir şekilde görüntülemek için "\xF0B7" öğesine tıklayın. Kırmızı çarpı resmi, oluşturulduktan sonra resim madde işareti resmi olarak ayarlanacaktır. Bunu değiştirmek için lütfen şunu kullanın:[`ImageData`](../imagedata/).

## Örnekler

Liste öğesi etiketleri için özel bir resim simgesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Mevcut liste düzeyi için bir resim madde işareti oluştur ve yerel bir dosya sisteminden bir resim ayarla
// Bu liste düzeyi için madde işaretlerinin gösterileceği simge olarak.
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

### Ayrıca bakınız

* class [ListLevel](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
