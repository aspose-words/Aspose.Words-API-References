---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName yöntemi"
linktitle: "get_ImageFileName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName yöntemi. C++'ta resmin kaydedileceği dosya adını (yol olmadan) alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/imagesavingargs/get_imagefilename/
---
## ImageSavingArgs::get_ImageFileName method


Görüntünün kaydedileceği dosya adını (yol olmadan) alır veya ayarlar.

```cpp
System::String Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName() const
```

## Açıklamalar


Bu özellik, HTML'ye dışa aktarım sırasında resim dosya adlarının nasıl oluşturulacağını yeniden tanımlamanıza olanak tanır.

Olay tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan dosya adını içerir. Resmi farklı bir dosyaya kaydetmek için bu özelliğin değerini değiştirebilirsiniz. Dosya adlarının benzersiz olması gerektiğini unutmayın.

Aspose.Words, HTML formatına dışa aktarırken gömülü her resim için otomatik olarak benzersiz bir dosya adı oluşturur. Resim dosya adının nasıl oluşturulacağı, belgeyi bir dosyaya mı yoksa bir akısa mı kaydettiğinize bağlıdır.

Bir belgeyi dosyaya kaydederken, oluşturulan resim dosya adı *%<document base file name>.<image number>.<extension>* şeklinde görünür.

Bir belgeyi akısa kaydederken, oluşturulan resim dosya adı *Aspose.Words.<document guid>.<image number>.<extension>* şeklinde görünür.

[ImageFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to HTML using the document file name, the [ImagesFolder](../../htmlsaveoptions/get_imagesfolder/) and [ImagesFolderAlias](../../htmlsaveoptions/get_imagesfolderalias/) properties.

## Ayrıca Bakınız

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
