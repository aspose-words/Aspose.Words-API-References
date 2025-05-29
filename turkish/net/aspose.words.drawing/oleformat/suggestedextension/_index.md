---
title: OleFormat.SuggestedExtension
linktitle: SuggestedExtension
articleTitle: SuggestedExtension
second_title: .NET için Aspose.Words
description: Gömülü nesnelerinizi etkili bir şekilde kaydetmek için ideal dosya uzantısını kolayca elde etmek amacıyla OleFormat SuggestedExtension özelliğini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words.drawing/oleformat/suggestedextension/
---
## OleFormat.SuggestedExtension property

Mevcut gömülü nesneyi bir dosyaya kaydetmek istiyorsanız, nesne için önerilen dosya uzantısını alır.

```csharp
public string SuggestedExtension { get; }
```

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
