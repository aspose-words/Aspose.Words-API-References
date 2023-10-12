---
title: Class OlePackage
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.OlePackage sınıf. OLE Paketi özelliklerine erişim sağlar.
type: docs
weight: 1160
url: /tr/net/aspose.words.drawing/olepackage/
---
## OlePackage class

OLE Paketi özelliklerine erişim sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Ole Nesneleriyle Çalışmak](https://docs.aspose.com/words/net/working-with-ole-objects/) dokümantasyon makalesi.

```csharp
public class OlePackage
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | OLE Paketinin görünen adını alır veya ayarlar. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | OLE Paketi dosya adını alır veya ayarlar. |

### Notlar

OLE paketi, OLE işleyicisi bilinmiyorsa gömülü nesneyi depolamanın eski ve "belgelenmemiş" bir yoludur. Windows 3.1, 95 ve 98 gibi ilk Windows sürümlerinde, her türlü veriyi belgeye gömmek için kullanılabilecek Packager.exe uygulaması vardı . Artık bu uygulama Windows'un dışında bırakıldı ancak MS Word ve diğer uygulamalar, OLE işleyicisi eksik veya bilinmiyorsa verileri gömmek için hala onu kullanıyor.

### Örnekler

Bir OLE nesnesinin belgeye nasıl eklendiğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// OLE nesneleri, kurulu başka bir uygulamayı kullanarak yerel dosya sistemindeki diğer dosyaları açmamıza olanak tanır
// işletim sistemimizde belge gövdesinde OLE nesnesini içeren şekle çift tıklayarak.
// Bu durumda harici dosyamız ZIP arşivi olacaktır.
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


