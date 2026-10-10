---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder metodu"
linktitle: "get_ImagesFolder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder metodu. Bir belgeyi HTML formatına dışa aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir. Varsayılan değer C++'ta boş bir dizedir."
type: docs
weight: 38000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolder/
---
## HtmlSaveOptions::get_ImagesFolder method


Bir belge HTML formatına dışa aktarılırken görüntülerin kaydedileceği fiziksel klasörü belirtir. Varsayılan değer boş bir dizedir.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder() const
```

## Açıklamalar


Bir [Document](../../../aspose.words/document/) belgesini HTML formatında kaydettiğinizde, Aspose.Words belgedeki tüm gömülü görüntüleri bağımsız dosyalar olarak kaydetmek zorundadır. [ImagesFolder](./) görüntülerin nereye kaydedileceğini belirtmenizi sağlar ve [ImagesFolderAlias](../get_imagesfolderalias/) görüntü URI'lerinin nasıl oluşturulacağını belirtmenize olanak tanır.

Bir belgeyi bir dosyaya kaydedip dosya adı sağlarsanız, Aspose.Words varsayılan olarak görüntüleri belge dosyasının kaydedildiği aynı klasöre kaydeder. Bu davranışı geçersiz kılmak için [ImagesFolder](./) kullanın.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words'un görüntüleri kaydedecek bir klasörü olmaz, ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, [ImagesFolder](./) özelliğinde erişilebilir bir klasör belirtmeniz veya [ImageSavingCallback](../get_imagesavingcallback/) olay işleyicisi aracılığıyla özel akışlar sağlamanız gerekir.

[ImagesFolder](./) tarafından belirtilen klasör mevcut değilse, otomatik olarak oluşturulacaktır.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where images should be saved.

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
