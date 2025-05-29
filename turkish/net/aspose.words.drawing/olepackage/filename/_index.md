---
title: OlePackage.FileName
linktitle: FileName
articleTitle: FileName
second_title: .NET için Aspose.Words
description: OLE paket dosya adlarını kolayca yönetmek için OlePackage FileName özelliğini keşfedin. Sorunsuz entegrasyon ve esneklikle veri işlemeyi geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/olepackage/filename/
---
## OlePackage.FileName property

OLE Paketi dosya adını alır veya ayarlar.

```csharp
public string FileName { get; set; }
```

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

* class [OlePackage](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
