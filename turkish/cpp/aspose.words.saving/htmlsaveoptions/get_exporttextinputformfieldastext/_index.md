---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText yöntemi"
linktitle: "get_ExportTextInputFormFieldAsText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText yöntemi. Metin giriş form alanlarının HTML veya MHTML'ye nasıl kaydedileceğini kontrol eder. Varsayılan değer C++'ta false'tur."
type: docs
weight: 28000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exporttextinputformfieldastext/
---
## HtmlSaveOptions::get_ExportTextInputFormFieldAsText method


Metin giriş form alanlarının HTML veya MHTML olarak nasıl kaydedileceğini denetler. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText() const
```

## Açıklamalar


**true** olarak ayarlandığında, metin giriş form alanlarını normal metin olarak dışa aktarır. **false** olarak ayarlandığında, Word metin giriş form alanlarını HTML'de INPUT öğeleri olarak dışa aktarır.

EPUB olarak dışa aktarılırken, bu formatın gereksinimleri nedeniyle metin giriş form alanları her zaman metin olarak kaydedilir.

## Örnekler



Bağlantılı görüntülerin .html olarak kaydedildikten sonra depolanacağı klasörün nasıl belirtileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Form alanlarını HTML giriş öğeleri yerine düz metin olarak dışa aktarmak için bir seçenek ayarlayın.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
