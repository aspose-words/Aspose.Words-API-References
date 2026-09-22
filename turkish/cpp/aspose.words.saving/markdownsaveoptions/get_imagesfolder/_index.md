---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder yöntemi"
linktitle: "get_ImagesFolder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder yöntemi. Bir belgeyi Markdown formatına dışa aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir. Varsayılan değer C++'da boş bir dizedir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolder/
---
## MarkdownSaveOptions::get_ImagesFolder method


Bir belgeyi [Markdown](../../../aspose.words/saveformat/) formatına dışa aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir. Varsayılan değer boş bir dizedir.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder() const
```

## Açıklamalar


[Document](../../../aspose.words/document/) belgesini [Markdown](../../../aspose.words/saveformat/) formatında kaydettiğinizde, Aspose.Words belgenin içine gömülü tüm görüntüleri bağımsız dosyalar olarak kaydetmek zorundadır. [ImagesFolder](./) görüntülerin nereye kaydedileceğini belirtmenizi sağlar.

Bir belgeyi bir dosyaya kaydedip dosya adı sağlarsanız, Aspose.Words varsayılan olarak görüntüleri belge dosyasının kaydedildiği aynı klasöre kaydeder. Bu davranışı geçersiz kılmak için [ImagesFolder](./) kullanın.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words görüntüleri kaydedecek bir klasöre sahip değildir, ancak yine de görüntüleri bir yerde kaydetmesi gerekir. Bu durumda, [ImagesFolder](./) özelliğinde erişilebilir bir klasör belirtmeniz gerekir.

[ImagesFolder](./) tarafından belirtilen klasör mevcut değilse, otomatik olarak oluşturulacaktır.

## Örnekler



Görüntü URI'lerini oluşturmak için kullanılan klasörün adının nasıl belirtileceğini gösterir.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->Writeln(u"Some image below:");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

System::String imagesFolder = System::IO::Path::Combine(get_ArtifactsDir(), u"ImagesDir");
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
// "ImagesFolder" özelliğini, yerel dosya sisteminde bir klasör atamak için kullanın
// Aspose.Words belgenin tüm bağlı görüntülerini kaydedecektir.
saveOptions->set_ImagesFolder(imagesFolder);
// "ImagesFolderAlias" özelliğini bu klasörü kullanmak için kullanın
// görüntü URI'lerini oluştururken görüntüler klasörünün adı yerine.
saveOptions->set_ImagesFolderAlias(u"http://example.com/images");

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

## Ayrıca Bakınız

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
