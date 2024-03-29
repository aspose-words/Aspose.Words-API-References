---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
articleTitle: CreatePictureBullet
second_title: Aspose.Words for .NET
description: ListLevel CreatePictureBullet yöntem. Geçerli liste düzeyi için resim madde işareti şeklini oluşturur C#'da.
type: docs
weight: 150
url: /tr/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

Geçerli liste düzeyi için resim madde işareti şeklini oluşturur.

```csharp
public void CreatePictureBullet()
```

## Notlar

Lütfen aklınızda bulundurun,[`NumberStyle`](../numberstyle/) şu şekilde ayarlanacak:Bullet ve [`NumberFormat`](../numberformat/) Resim işaretini düzgün bir şekilde görüntülemek için "\xF0B7" olarak ayarlayın. Kırmızı haç resmi, oluşturma sırasında resim işaret resmi olarak ayarlanacaktır. Değiştirmek için lütfen şunu kullanın:[`ImageData`](../imagedata/).

## Örnekler

Liste öğesi etiketleri için özel bir görüntü simgesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Geçerli liste düzeyi için bir resim işareti oluşturun ve yerel dosya sisteminden bir resim ayarlayın
// bu liste düzeyi için madde işaretlerinin görüntüleyeceği simge olarak.
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
