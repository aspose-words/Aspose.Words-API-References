---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Metin girişi form alanlarının HTML veya MHTMLye nasıl kaydedileceğini kontrol eder. Varsayılan değerYANLIŞ .
type: docs
weight: 260
url: /tr/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Metin girişi form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer:`YANLIŞ` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

### Notlar

olarak ayarlandığında`doğru` , metin giriş formu alanlarını normal metin olarak dışa aktarır. Ne zaman`YANLIŞ`, Word metni giriş formu alanlarını HTML'deki INPUT öğeleri olarak dışa aktarır.

EPUB'a dışa aktarırken, metin giriş formu alanları bu formatın gereklilikleri nedeniyle nedeniyle her zaman metin olarak kaydedilir.

### Örnekler

Bağlantılı görsellerin .html'ye kaydedildikten sonra saklanacağı klasörün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Form alanlarını HTML giriş öğeleri yerine düz metin olarak dışa aktarmak için bir seçenek belirleyin.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


