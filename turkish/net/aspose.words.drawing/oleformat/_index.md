---
title: OleFormat Class
linktitle: OleFormat
articleTitle: OleFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.OleFormat sınıf. Bir OLE nesnesinin veya ActiveX denetiminin verilerine erişim sağlar C#'da.
type: docs
weight: 1150
url: /tr/net/aspose.words.drawing/oleformat/
---
## OleFormat class

Bir OLE nesnesinin veya ActiveX denetiminin verilerine erişim sağlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Ole Nesneleriyle Çalışmak](https://docs.aspose.com/words/net/working-with-ole-objects/) dokümantasyon makalesi.

```csharp
public class OleFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | OLE nesnesine olan bağlantının Microsoft Word'de otomatik olarak güncelleştirilip güncelleştirilmeyeceğini belirtir. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | OLE nesnesinin CLSID'sini alır. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | OLE nesnesinin simge başlığını alır. |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | İadeler`doğru` OLE nesnesi bağlıysa (ne zaman[`SourceFullName`](./sourcefullname/) belirtildi). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | OLE nesnesine olan bağlantının güncellemelere karşı kilitlenip kilitlenmediğini belirtir. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | Alır[`OleControl`](./olecontrol/) Bu OLE nesnesi bir ActiveX denetimi ise nesneler. Aksi halde bu özellik null. olur |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | OLE nesnesinin çizim yönünü alır. Ne zaman`doğru` OLE nesnesi bir simge olarak görüntülenir. Ne zaman`YANLIŞ` OLE nesnesi content. olarak görüntülenir. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | Erişim sağla[`OlePackage`](../olepackage/) OLE nesnesi bir OLE Paketi ise. Döndürür`hükümsüz` aksi halde. |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | OLE nesnesinin ProgID'sini alır veya ayarlar. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | Bağlantılı OLE nesnesine ilişkin kaynak dosyanın yolunu ve adını alır veya ayarlar. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | Kaynak dosyanın bağlanan kısmını tanımlamak için kullanılan bir dizeyi alır veya ayarlar. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | Geçerli gömülü nesneyi bir dosyaya kaydetmek istiyorsanız, önerilen dosya uzantısını alır. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | Geçerli gömülü nesneyi bir dosyaya kaydetmek istiyorsanız, önerilen dosya adını alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(*string*) | OLE nesnesi veri girişini alır. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | OLE nesnesinin ham verilerini alır. |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(*Stream*) | Gömülü nesnenin verilerini belirtilen akışa kaydeder. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(*string*) | Gömülü nesnenin verilerini belirtilen adda bir dosyaya kaydeder. |

## Notlar

Kullan[`OleFormat`](../shape/oleformat/)OLE nesnesinin verilerine erişme özelliği. Örneklerini oluşturmazsınız`OleFormat` doğrudan sınıf.

## Örnekler

Katıştırılmış OLE nesnelerinin dosyalara nasıl çıkartılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// İlk şekildeki OLE nesnesi bir Microsoft Excel elektronik tablosudur.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Nesnemiz ne otomatik güncelleniyor ne de güncellemelerden kilitli.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// OLE nesnesini yerel dosya sistemindeki bir dosyaya kaydetmeyi planlıyorsak,
// Dosyaya hangi dosya uzantısının uygulanacağını belirlemek için "SuggestedExtension" özelliğini kullanabiliriz.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Aşağıda bir OLE nesnesini yerel dosya sistemindeki bir dosyaya kaydetmenin iki yolu verilmiştir.
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
