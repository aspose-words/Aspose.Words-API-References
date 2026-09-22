---
title: "Aspose::Words::Saving::SaveOptions::get_TempFolder yöntemi"
linktitle: "get_TempFolder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::SaveOptions::get_TempFolder yöntemi. DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik null'dur ve C++'da geçici dosya kullanılmaz."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.saving/saveoptions/get_tempfolder/
---
## SaveOptions::get_TempFolder method


DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_TempFolder() const
```

## Açıklamalar


Aspose.Words bir belgeyi kaydettiğinde, geçici iç yapılar oluşturması gerekir. Varsayılan olarak, bu iç yapılar bellekte oluşturulur ve belge kaydedilirken bellek kullanımı kısa bir süre için artar. Kaydetme tamamlandığında, bellek serbest bırakılır ve çöp toplayıcı tarafından geri kazanılır.

[TempFolder](./) kullanarak geçici bir klasör belirtmek, Aspose.Words'ün iç yapıları bellek yerine geçici dosyalarda tutmasını sağlar. Bu, kaydetme sırasında bellek kullanımını azaltır, ancak kaydetme performansını düşürür.

Klasör mevcut olmalı ve yazılabilir olmalıdır, aksi takdirde bir istisna fırlatılacaktır.

Aspose.Words, kaydetme tamamlandığında tüm geçici dosyaları otomatik olarak siler.

## Örnekler



Bir belgeyi kaydederken belleğin yerine sabit sürücünün nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Bir belgeyi kaydettiğimizde, çeşitli öğeler kaydetme işlemi gerçekleşirken geçici olarak bellekte depolanır.
// Bunun yerine yerel dosya sisteminde geçici bir klasör kullanmak için bu seçeneği kullanabiliriz,
// bu, uygulamamızın bellek yükünü azaltacaktır.
auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// Belirtilen geçici klasör, kaydetme işleminden önce yerel dosya sisteminde mevcut olmalıdır.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.TempFolder.doc", options);

// Klasör, yükleme işleminden kalan içerik olmadan kalıcı olacaktır.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Ayrıca Bakınız

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
