---
title: SaveOptions.UpdateSdtContent
second_title: Aspose.Words for .NET API Referansı
description: SaveOptions mülk. İçeriğin olup olmadığını belirleyen değeri alır veya ayarlar.StructuredDocumentTag kaydetmeden önce güncellenir.
type: docs
weight: 200
url: /tr/net/aspose.words.saving/saveoptions/updatesdtcontent/
---
## SaveOptions.UpdateSdtContent property

İçeriğin olup olmadığını belirleyen değeri alır veya ayarlar.[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) kaydetmeden önce güncellenir.

```csharp
public bool UpdateSdtContent { get; set; }
```

### Notlar

Varsayılan değer`doğru` .

### Örnekler

Bir belgeyi PDF'ye kaydederken yapılandırılmış belge etiketlerinin nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();

// Bir açılır liste yapılandırılmış belge etiketi ekleyin.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
tag.ListItems.Add(new SdtListItem("Value 1"));
tag.ListItems.Add(new SdtListItem("Value 2"));
tag.ListItems.Add(new SdtListItem("Value 3"));

// Açılır liste şu anda varsayılan metin olarak "Bir öğe seçin"i gösteriyor.
// Etiketi almak için "SelectedValue" özelliğini liste öğelerinden birine ayarlayın
// varsayılan metin yerine o liste öğesinin değerini göster.
tag.ListItems.SelectedValue = tag.ListItems[1];

doc.FirstSection.Body.AppendChild(tag);

// Belgenin "Kaydet" yöntemine geçmek için bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye kaydetme şeklini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Yapılandırılmış belge etiketlerini güncellememek için "UpdateSdtContent" özelliğini "false" olarak ayarlayın
// belgeyi PDF'ye kaydederken. Varsayılan değerlerini inşaat sırasındaki gibi gösterecekler.
// Etiketlerin PDF'de güncellenmiş değerleri gösterdiğinden emin olmak için "UpdateSdtContent" özelliğini "true" olarak ayarlayın.
options.UpdateSdtContent = updateSdtContent;

doc.Save(ArtifactsDir + "StructuredDocumentTag.UpdateSdtContent.pdf", options);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../saveoptions/)
* toplantı [Aspose.Words](../../../)


