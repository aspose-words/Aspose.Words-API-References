---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words for .NET
description: OleFormat OlePackage mülk. Erişim sağlaOlePackage OLE nesnesi bir OLE Paketi ise. Döndürürhükümsüz aksi halde C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Erişim sağla[`OlePackage`](../../olepackage/) OLE nesnesi bir OLE Paketi ise. Döndürür`hükümsüz` aksi halde.

```csharp
public OlePackage OlePackage { get; }
```

## Notlar

OLE Paketi, bir Windows sisteminin OLE kayıt defterinde bulunmayan herhangi bir dosya biçiminin, bir belgeye neredeyse her şeyin gömülmesine olanak tanıyan genel bir pakete sarılmasına olanak tanıyan eski bir teknolojidir. Bkz.[`OlePackage`](../../olepackage/) daha fazla bilgi için yazın.

## Örnekler

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

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
