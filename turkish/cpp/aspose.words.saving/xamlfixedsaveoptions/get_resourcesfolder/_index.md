---
title: "Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder metodu"
linktitle: "get_ResourcesFolder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder metodu. Bir belge sabit sayfa Xaml formatına dışa aktarılırken kaynakların (görseller ve yazı tipleri) kaydedildiği fiziksel klasörü belirtir. Varsayılan değer C++'ta null'dır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/xamlfixedsaveoptions/get_resourcesfolder/
---
## XamlFixedSaveOptions::get_ResourcesFolder method


Bir belge sabit sayfa Xaml formatına dışa aktarılırken kaynakların (görseller ve yazı tipleri) kaydedildiği fiziksel klasörü belirtir. Varsayılan **null**.

```cpp
System::String Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder() const
```

## Açıklamalar


Bir [Document](../../../aspose.words/document/) belgesini sabit sayfa Xaml formatında kaydettiğinizde, Aspose.Words belgedeki tüm gömülü görselleri bağımsız dosyalar olarak kaydetmek zorundadır. [ResourcesFolder](./) görsellerin nerede kaydedileceğini belirtmenizi sağlar ve [ResourcesFolderAlias](../get_resourcesfolderalias/) görsel URI'lerinin nasıl oluşturulacağını belirtmenize olanak tanır.

Bir belgeyi bir dosyaya kaydedip dosya adı sağlarsanız, Aspose.Words varsayılan olarak görüntüleri belgenin kaydedildiği aynı klasöre kaydeder. Bu davranışı geçersiz kılmak için [ResourcesFolder](./) kullanın.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words görüntüleri kaydedecek bir klasöre sahip değildir, ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, [ResourcesFolder](./) özelliğini kullanarak erişilebilir bir klasör belirtmeniz gerekir.

## Ayrıca Bakınız

* Class [XamlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
