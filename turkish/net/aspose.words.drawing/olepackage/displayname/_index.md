---
title: OlePackage.DisplayName
linktitle: DisplayName
articleTitle: DisplayName
second_title: .NET için Aspose.Words
description: OLE Paketi görüntü adlarını kolayca yönetmek için OlePackage DisplayName özelliğini keşfedin. Bu önemli özellik ile veri organizasyonunuzu geliştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/olepackage/displayname/
---
## OlePackage.DisplayName property

OLE Paketi görüntü adını alır veya ayarlar.

```csharp
public string DisplayName { get; set; }
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
