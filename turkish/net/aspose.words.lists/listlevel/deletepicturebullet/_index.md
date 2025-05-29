---
title: ListLevel.DeletePictureBullet
linktitle: DeletePictureBullet
articleTitle: DeletePictureBullet
second_title: .NET için Aspose.Words
description: ListLevel DeletePictureBullet yöntemiyle mevcut liste seviyenizden resim madde işaretlerini zahmetsizce kaldırın. Belge biçimlendirmenizi bugün basitleştirin!
type: docs
weight: 160
url: /tr/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

Mevcut liste düzeyi için resim madde işaretini siler.

```csharp
public void DeletePictureBullet()
```

## Notlar

Silindikten sonra varsayılan madde işareti gösterilecektir.

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
