---
title: Class OleFormat
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.OleFormat sınıf. Bir OLE nesnesinin veya ActiveX denetiminin verilerine erişim sağlar.
type: docs
weight: 1020
url: /tr/net/aspose.words.drawing/oleformat/
---
## OleFormat class

Bir OLE nesnesinin veya ActiveX denetiminin verilerine erişim sağlar.

```csharp
public class OleFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AutoUpdate](../../aspose.words.drawing/oleformat/autoupdate/) { get; set; } | OLE nesnesine olan bağlantının Microsoft Word'de otomatik olarak güncellenip güncellenmediğini belirtir. |
| [Clsid](../../aspose.words.drawing/oleformat/clsid/) { get; } | OLE nesnesinin CLSID'sini alır. |
| [IconCaption](../../aspose.words.drawing/oleformat/iconcaption/) { get; } | OLE nesnesinin simge başlığını alır. |
| [IsLink](../../aspose.words.drawing/oleformat/islink/) { get; } | OLE nesnesi bağlıysa (ne zaman[`SourceFullName`](./sourcefullname/) belirtilir). |
| [IsLocked](../../aspose.words.drawing/oleformat/islocked/) { get; set; } | OLE nesnesine olan bağlantının güncellemelerden kilitlenip kilitlenmediğini belirtir. |
| [OleControl](../../aspose.words.drawing/oleformat/olecontrol/) { get; } | Alır[`OleControl`](./olecontrol/) Bu OLE nesnesi bir ActiveX denetimiyse, nesneler. Aksi takdirde bu özellik null. olur. |
| [OleIcon](../../aspose.words.drawing/oleformat/oleicon/) { get; } | OLE nesnesinin çizim yönünü alır. Ne zaman **doğru** , OLE nesnesi bir simge olarak görüntülenir. Ne zaman **yanlış** , OLE nesnesi içerik olarak görüntülenir. |
| [OlePackage](../../aspose.words.drawing/oleformat/olepackage/) { get; } | Erişim sağlayın[`OlePackage`](../olepackage/) OLE nesnesi bir OLE Paketi ise. Aksi takdirde null döndürür. |
| [ProgId](../../aspose.words.drawing/oleformat/progid/) { get; set; } | OLE nesnesinin ProgID'sini alır veya ayarlar. |
| [SourceFullName](../../aspose.words.drawing/oleformat/sourcefullname/) { get; set; } | Bağlantılı OLE nesnesi için kaynak dosyanın yolunu ve adını alır veya ayarlar. |
| [SourceItem](../../aspose.words.drawing/oleformat/sourceitem/) { get; set; } | Kaynak dosyanın bağlanmakta olan bölümünü tanımlamak için kullanılan bir dize alır veya ayarlar. |
| [SuggestedExtension](../../aspose.words.drawing/oleformat/suggestedextension/) { get; } | Bir dosyaya kaydetmek istiyorsanız, mevcut gömülü nesne için önerilen dosya uzantısını alır. |
| [SuggestedFileName](../../aspose.words.drawing/oleformat/suggestedfilename/) { get; } | Bir dosyaya kaydetmek istiyorsanız, geçerli gömülü nesne için önerilen dosya adını alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetOleEntry](../../aspose.words.drawing/oleformat/getoleentry/)(string) | OLE nesne veri girişini alır. |
| [GetRawData](../../aspose.words.drawing/oleformat/getrawdata/)() | OLE nesnesi ham verilerini alır. |
| [Save](../../aspose.words.drawing/oleformat/save/#save)(Stream) | Gömülü nesnenin verilerini belirtilen akışa kaydeder. |
| [Save](../../aspose.words.drawing/oleformat/save/#save_1)(string) | Katıştırılmış nesnenin verilerini belirtilen ada sahip bir dosyaya kaydeder. |

### Notlar

Kullan[`OleFormat`](../shape/oleformat/) bir OLE nesnesinin verilerine erişme özelliği. `OleFormat` doğrudan sınıf.

### Örnekler

Gömülü OLE nesnelerinin dosyalara nasıl ayıklanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// İlk şekildeki OLE nesnesi bir Microsoft Excel elektronik tablosudur.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Nesnemiz ne otomatik güncelleme yapıyor ne de güncellemelere kilitleniyor.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// OLE nesnesini yerel dosya sistemindeki bir dosyaya kaydetmeyi planlıyorsak,
// Dosyaya hangi dosya uzantısının uygulanacağını belirlemek için "Önerilen Uzantı" özelliğini kullanabiliriz.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Aşağıda, bir OLE nesnesini yerel dosya sistemindeki bir dosyaya kaydetmenin iki yolu bulunmaktadır.
// 1 - Akış yoluyla kaydedin:
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


