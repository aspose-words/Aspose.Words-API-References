---
title: OleFormat.Save
linktitle: Save
articleTitle: Save
second_title: .NET için Aspose.Words
description: Seçtiğiniz akışta gömülü nesne verilerini verimli bir şekilde depolamak için OleFormat Save yöntemini keşfedin. Veri yönetimini kolaylıkla geliştirin!
type: docs
weight: 160
url: /tr/net/aspose.words.drawing/oleformat/save/
---
## Save(*Stream*) {#save}

Gömülü nesnenin verilerini belirtilen akışa kaydeder.

```csharp
public void Save(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Nesne verilerinin nereye kaydedileceği. |

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidOperationException | Bağlantılı bir nesneyi kaydetmeye çalıştığınızda fırlatır. |

## Notlar

Akışı bertaraf etmek arayanın sorumluluğundadır.

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

---

## Save(*string*) {#save_1}

Gömülü nesnenin verilerini belirtilen adla bir dosyaya kaydeder.

```csharp
public void Save(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | OLE nesnesi verilerinin kaydedileceği dosyanın adı. |

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidOperationException | Bağlantılı bir nesneyi kaydetmeye çalıştığınızda fırlatır. |

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
