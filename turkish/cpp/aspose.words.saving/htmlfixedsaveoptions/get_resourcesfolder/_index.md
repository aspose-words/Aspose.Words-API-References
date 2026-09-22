---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder yöntemi"
linktitle: "get_ResourcesFolder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder yöntemi. Bir belgeyi Html formatına dışa aktarırken kaynakların (görseller, yazı tipleri, css) kaydedildiği fiziksel klasörü belirtir. Varsayılan değer C++'de null'dur."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.saving/htmlfixedsaveoptions/get_resourcesfolder/
---
## HtmlFixedSaveOptions::get_ResourcesFolder method


Bir belge HTML formatına dışa aktarılırken kaynakların (görseller, yazı tipleri, css) kaydedileceği fiziksel klasörü belirtir. Varsayılan **null**.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder() const
```

## Açıklamalar


Yalnızca [ExportEmbeddedImages](../get_exportembeddedimages/) özelliği **false** olduğunda etkili olur.

Bir [Document](../../../aspose.words/document/) belgesini Html formatında kaydettiğinizde, Aspose.Words belgedeki tüm gömülü görüntüleri bağımsız dosyalar olarak kaydetmek zorundadır. [ResourcesFolder](./) görüntülerin nereye kaydedileceğini belirtmenizi sağlar ve [ResourcesFolderAlias](../get_resourcesfolderalias/) görüntü URI'lerinin nasıl oluşturulacağını belirtmenize olanak tanır.

Bir belgeyi bir dosyaya kaydedip dosya adı sağlarsanız, Aspose.Words varsayılan olarak görüntüleri belgenin kaydedildiği aynı klasöre kaydeder. Bu davranışı geçersiz kılmak için [ResourcesFolder](./) kullanın.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words görüntüleri kaydedecek bir klasöre sahip değildir, ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, [ResourcesFolder](./) özelliğini kullanarak erişilebilir bir klasör belirtmeniz gerekir.

## Ayrıca Bakınız

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
