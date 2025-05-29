---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
articleTitle: ExportTextInputFormFieldAsText
second_title: .NET için Aspose.Words
description: HtmlSaveOptions ExportTextInputFormFieldAsText özelliğinin, sorunsuz HTML veya MHTML kaydı için metin girişi form alanlarını nasıl optimize ettiğini keşfedin. Dışa aktarma sürecinizi geliştirin!
type: docs
weight: 260
url: /tr/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Metin girişi form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer`YANLIŞ` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## Notlar

Ayarlandığında`doğru` , metin girişi form alanlarını normal metin olarak dışa aktarır. `YANLIŞ`, Word metin girişi form alanlarını HTML'de GİRİŞ öğeleri olarak dışa aktarır.

EPUB'a aktarırken, metin girişi form alanları bu formatın gereklilikleri nedeniyle her zaman metin olarak kaydedilir.

## Örnekler

Bağlantılı görsellerin .html olarak kaydedildikten sonra saklanacağı klasörün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Form alanlarını HTML giriş öğeleri yerine düz metin olarak dışa aktarmak için bir seçenek ayarlayın.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
