---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: .NET için Aspose.Words
description: OLE nesneleri için OlePackage özelliklerine zahmetsizce erişin. OLE Paketleri ile sorunsuz entegrasyon sağlayın ve veri işleme yeteneklerinizi geliştirin.
type: docs
weight: 80
url: /tr/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Erişim sağlayın[`OlePackage`](../../olepackage/) OLE nesnesi bir OLE Paketi ise. Döndürür`hükümsüz` aksi takdirde.

```csharp
public OlePackage OlePackage { get; }
```

## Notlar

OLE Paketi, bir Windows sisteminin OLE kayıt defterinde bulunmayan herhangi bir dosya biçimini, neredeyse her şeyi bir belgeye yerleştirmeye izin veren genel bir pakete sarmaya olanak tanıyan eski bir teknolojidir. Bkz.[`OlePackage`](../../olepackage/) daha fazla bilgi için yazın.

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

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
