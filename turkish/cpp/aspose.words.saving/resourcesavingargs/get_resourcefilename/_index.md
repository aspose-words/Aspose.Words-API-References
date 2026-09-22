---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName yöntemi"
linktitle: "get_ResourceFileName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName yöntemi. C++'de kaynağın kaydedileceği dosya adını (yol olmadan) alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/resourcesavingargs/get_resourcefilename/
---
## ResourceSavingArgs::get_ResourceFileName method


Kaynağın kaydedileceği dosya adını (yol olmadan) alır veya ayarlar.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName() const
```

## Açıklamalar


Bu özellik, sabit sayfa HTML, SVG veya Markdown dışa aktarımı sırasında kaynak dosya adlarının nasıl oluşturulduğunu yeniden tanımlamanıza olanak tanır.

Olay tetiklendiğinde, bu özellik Aspose.Words tarafından oluşturulan dosya adını içerir. Kaynağı farklı bir dosyaya kaydetmek için bu özelliğin değerini değiştirebilirsiniz. Dosya adlarının benzersiz olması gerektiğini unutmayın.

Aspose.Words, sabit sayfa HTML, SVG veya Markdown formatına dışa aktarırken her kaynak için otomatik olarak benzersiz bir dosya adı oluşturur. Kaynak dosya adının nasıl oluşturulacağı, belgeyi bir dosyaya mı yoksa bir akışa mı kaydettiğinize bağlıdır.

Bir belgeyi dosyaya kaydederken, oluşturulan kaynak dosya adı *%<document base file name>.<image number>.<extension>* şeklinde görünür.

Bir belgeyi akışa kaydederken, oluşturulan kaynak dosya adı *Aspose.Words.<document guid>.<image number>.<extension>* şeklinde görünür.

[ResourceFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [ResourcesFolder](../../htmlfixedsaveoptions/get_resourcesfolder/) or [ResourcesFolder](../../svgsaveoptions/get_resourcesfolder/) and [ResourcesFolderAlias](../../htmlfixedsaveoptions/get_resourcesfolderalias/) or [ResourcesFolderAlias](../../svgsaveoptions/get_resourcesfolderalias/) or [ImagesFolder](../../markdownsaveoptions/get_imagesfolder/) or [ImagesFolderAlias](../../markdownsaveoptions/get_imagesfolderalias/) properties.

## Ayrıca Bakınız

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
