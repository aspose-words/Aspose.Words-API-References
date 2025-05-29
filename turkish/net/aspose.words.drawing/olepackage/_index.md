---
title: OlePackage Class
linktitle: OlePackage
articleTitle: OlePackage
second_title: .NET için Aspose.Words
description: OLE Paketi özelliklerini kolayca yönetmek ve belge işleme yeteneklerinizi geliştirmek için Aspose.Words.Drawing.OlePackage sınıfını keşfedin.
type: docs
weight: 1540
url: /tr/net/aspose.words.drawing/olepackage/
---
## OlePackage class

OLE Paketi özelliklerine erişime izin verir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Ole Nesneleriyle Çalışma](https://docs.aspose.com/words/net/working-with-ole-objects/) belgeleme makalesi.

```csharp
public class OlePackage
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | OLE Paketi görüntü adını alır veya ayarlar. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | OLE Paketi dosya adını alır veya ayarlar. |

## Notlar

OLE paketi, OLE işleyicisi bilinmiyorsa gömülü nesneyi depolamak için kullanılan eski ve "belgelenmemiş" bir yoldur. Windows 3.1, 95 ve 98 gibi erken Windows sürümlerinde, herhangi bir veri türünü belgeye gömmek için kullanılabilen Packager.exe uygulaması vardı. Şimdi bu uygulama Windows'tan hariç tutulmuştur ancak MS Word ve diğer uygulamalar, OLE işleyicisi eksik veya bilinmiyorsa veri gömmek için hala bunu kullanmaktadır.

## Örnekler

Bir OLE nesnesinin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE nesneleri, yerel dosya sistemindeki diğer dosyaları başka bir yüklü uygulamayı kullanarak açmamıza olanak tanır
// İşletim sistemimizde, belge gövdesinde OLE nesnesini içeren şekle çift tıklayarak.
// Bu durumda harici dosyamız bir ZIP arşivi olacaktır.
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
