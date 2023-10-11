---
title: OlePackage.DisplayName
second_title: Aspose.Words for .NET API Referansı
description: OlePackage mülk. OLE Paketinin görünen adını alır veya ayarlar.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/olepackage/displayname/
---
## OlePackage.DisplayName property

OLE Paketinin görünen adını alır veya ayarlar.

```csharp
public string DisplayName { get; set; }
```

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

* class [OlePackage](../)
* ad alanı [Aspose.Words.Drawing](../../olepackage/)
* toplantı [Aspose.Words](../../../)


