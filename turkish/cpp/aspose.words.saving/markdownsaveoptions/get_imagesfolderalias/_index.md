---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias yöntemi"
linktitle: "get_ImagesFolderAlias"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias yöntemi. Bir belgeye yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan değer C++'da boş bir dizedir."
type: docs
weight: 5500
url: /tr/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolderalias/
---
## MarkdownSaveOptions::get_ImagesFolderAlias method


Belgeye yazılan görüntü URI'lerini oluşturmak için kullanılan klasör adını belirtir. Varsayılan boş bir dizedir.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias() const
```

## Açıklamalar


Bir [Document](../../../aspose.words/document/) belgesini [Markdown](../../../aspose.words/saveformat/) formatında kaydettiğinizde, Aspose.Words belgenin içine gömülü tüm görüntüleri bağımsız dosyalar olarak kaydetmek zorundadır. [ImagesFolder](../get_imagesfolder/) görüntülerin nereye kaydedileceğini belirtmenizi sağlar ve [ImagesFolderAlias](./) görüntü URI'lerinin nasıl oluşturulacağını belirtmenize olanak tanır.

Eğer [ImagesFolderAlias](./) boş bir dize değilse, Markdown'a yazılan görüntü URI'si *ImagesFolderAlias + <image file name>* şeklinde olur.

Eğer [ImagesFolderAlias](./) boş bir dize ise, Markdown'a yazılan görüntü URI'si *ImagesFolder + <image file name>* şeklinde olur.

Eğer [ImagesFolderAlias](./) '.' (nokta) olarak ayarlanmışsa, diğer seçeneklerden bağımsız olarak görüntü dosya adı yol olmadan Markdown'a yazılır.

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
