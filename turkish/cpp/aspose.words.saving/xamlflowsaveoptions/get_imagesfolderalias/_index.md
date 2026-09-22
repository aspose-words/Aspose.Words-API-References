---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias metodu"
linktitle: "get_ImagesFolderAlias"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias metodu. XAML belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan değer C++'ta boş bir dizedir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolderalias/
---
## XamlFlowSaveOptions::get_ImagesFolderAlias method


XAML belgesine yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan değer boş bir dizedir.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias() const
```

## Açıklamalar


Bir [Document](../../../aspose.words/document/) belgesini XAML formatında kaydettiğinizde, Aspose.Words tüm gömülü görüntüleri bağımsız dosyalar olarak kaydetmek zorundadır. [ImagesFolder](../get_imagesfolder/) görüntülerin nereye kaydedileceğini belirtmenizi sağlar ve [ImagesFolderAlias](./) görüntü URI'lerinin nasıl oluşturulacağını belirtmenize olanak tanır.

Eğer [ImagesFolderAlias](./) boş bir dize değilse, XAML'e yazılan görüntü URI'si *ImagesFolderAlias + <image file name>* olacaktır.

Eğer [ImagesFolderAlias](./) boş bir dize ise, XAML'e yazılan görüntü URI'si *ImagesFolder + <image file name>* olacaktır.

Eğer [ImagesFolderAlias](./) '.' (nokta) olarak ayarlanmışsa, diğer seçenekler ne olursa olsun görüntü dosya adı yol olmadan XAML'e yazılacaktır.

## Ayrıca Bakınız

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
