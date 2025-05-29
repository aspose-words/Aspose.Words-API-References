---
title: OleFormat Class
linktitle: OleFormat
articleTitle: OleFormat
second_title: .NET için Aspose.Words
description: OLE nesnelerine ve ActiveX denetimlerine kesintisiz erişim için Aspose.Words.Drawing.OleFormat sınıfını keşfedin ve belge işleme yeteneklerinizi geliştirin.
type: docs
weight: 1530
url: /tr/net/aspose.words.drawing/oleformat/
---
## OleFormat class

Bir OLE nesnesinin veya ActiveX denetiminin verilerine erişim sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Ole Nesneleriyle Çalışma](https://docs.aspose.com/words/net/working-with-ole-objects/) belgeleme makalesi.

```csharp
public class OleFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | OLE nesnesine olan bağlantının Microsoft Word'de otomatik olarak güncellenip güncellenmeyeceğini belirtir. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | OLE nesnesinin CLSID'sini alır. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | OLE nesnesinin simge başlığını alır. |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | Geri Döndürür`doğru` OLE nesnesi bağlıysa (ne zaman[`SourceFullName`](./sourcefullname/) belirtilmiştir). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | OLE nesnesine olan bağlantının güncellemelere karşı kilitli olup olmadığını belirtir. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | Alır[`OleControl`](./olecontrol/) Bu OLE nesnesi bir ActiveX denetimiyse nesneler. Aksi takdirde bu özellik null'dır. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | OLE nesnesinin çizim yönünü alır.`doğru` OLE nesnesi bir simge olarak görüntülenir. `YANLIŞ` , OLE nesnesi içerik olarak görüntülenir. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | Erişim sağlayın[`OlePackage`](../olepackage/) OLE nesnesi bir OLE Paketi ise. Döndürür`hükümsüz` aksi takdirde. |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | OLE nesnesinin ProgID'sini alır veya ayarlar. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | Bağlantılı OLE nesnesi için kaynak dosyasının yolunu ve adını alır veya ayarlar. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | Bağlantı kurulan kaynak dosyanın bölümünü tanımlamak için kullanılan bir dizeyi alır veya ayarlar. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | Mevcut gömülü nesneyi bir dosyaya kaydetmek istiyorsanız, nesne için önerilen dosya uzantısını alır. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | Mevcut gömülü nesneyi bir dosyaya kaydetmek istiyorsanız, nesne için önerilen dosya adını alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(*string*) | OLE nesnesi veri girişini alır. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | OLE nesnesinin ham verilerini alır. |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(*Stream*) | Gömülü nesnenin verilerini belirtilen akışa kaydeder. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(*string*) | Gömülü nesnenin verilerini belirtilen adla bir dosyaya kaydeder. |

## Notlar

Kullanın[`OleFormat`](../shape/oleformat/) Bir OLE nesnesinin verilerine erişmek için özellik. Örnekleri oluşturmazsınız`OleFormat` sınıfa doğrudan.

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
