---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder metodu"
linktitle: "get_ImagesFolder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder metodu. Bir belge XAML formatına dışa aktarıldığında görüntülerin kaydedildiği fiziksel klasörü belirtir. Varsayılan değer C++'ta boş bir dizedir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolder/
---
## XamlFlowSaveOptions::get_ImagesFolder method


Bir belge XAML formatına dışa aktarıldığında görüntülerin kaydedildiği fiziksel klasörü belirtir. Varsayılan değer boş bir dizedir.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder() const
```

## Açıklamalar


Bir [Document](../../../aspose.words/document/) belgesini XAML formatında kaydettiğinizde, Aspose.Words tüm gömülü görüntüleri bağımsız dosyalar olarak kaydetmek zorundadır. [ImagesFolder](./) görüntülerin nereye kaydedileceğini belirtmenizi sağlar ve [ImagesFolderAlias](../get_imagesfolderalias/) görüntü URI'lerinin nasıl oluşturulacağını belirtmenize olanak tanır.

Bir belgeyi bir dosyaya kaydedip dosya adı sağlarsanız, Aspose.Words varsayılan olarak görüntüleri belge dosyasının kaydedildiği aynı klasöre kaydeder. Bu davranışı geçersiz kılmak için [ImagesFolder](./) kullanın.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words'un görüntüleri kaydedecek bir klasörü olmaz, ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, [ImagesFolder](./) özelliğinde erişilebilir bir klasör belirtmeniz veya [ImageSavingCallback](../get_imagesavingcallback/) olay işleyicisi aracılığıyla özel akışlar sağlamanız gerekir.

## Ayrıca Bakınız

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
