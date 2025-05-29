---
title: OleFormat.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: .NET için Aspose.Words
description: OleFormat IsLocked özelliğini keşfedin, OLE nesne bağlantılarını kontrol edin ve istenmeyen güncellemeleri önleyerek veri bütünlüğünü artırın. Şimdi daha fazlasını öğrenin!
type: docs
weight: 50
url: /tr/net/aspose.words.drawing/oleformat/islocked/
---
## OleFormat.IsLocked property

OLE nesnesine olan bağlantının güncellemelere karşı kilitli olup olmadığını belirtir.

```csharp
public bool IsLocked { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ`.

## Örnekler

Gömülü OLE nesnelerinin dosyalara nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// İlk şekildeki OLE nesnesi bir Microsoft Excel elektronik tablosudur.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Nesnemiz ne otomatik güncelleniyor ne de güncellemelere kapalı.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// OLE nesnesini yerel dosya sistemindeki bir dosyaya kaydetmeyi planlıyorsak,
// Dosyaya hangi dosya uzantısının uygulanacağını belirlemek için "SuggestedExtension" özelliğini kullanabiliriz.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Aşağıda bir OLE nesnesini yerel dosya sistemindeki bir dosyaya kaydetmenin iki yolu bulunmaktadır.
// 1 - Bir akış aracılığıyla kaydedin:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Doğrudan bir dosya adına kaydedin:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Ayrıca bakınız

* class [OleFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
