---
title: "Aspose::Words::Loading::LoadOptions::get_TempFolder yöntemi"
linktitle: "get_TempFolder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_TempFolder yöntemi. Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik null'dur ve C++'da geçici dosya kullanılmaz."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.loading/loadoptions/get_tempfolder/
---
## LoadOptions::get_TempFolder method


Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik **null**'dır ve geçici dosya kullanılmaz.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_TempFolder() const
```

## Açıklamalar


Klasör mevcut olmalı ve yazılabilir olmalıdır, aksi takdirde bir istisna fırlatılacaktır.

Aspose.Words okuma tamamlandığında tüm geçici dosyaları otomatik olarak siler.

## Örnekler



Geçici dosyalar kullanarak bir belgeyi nasıl yükleyeceğinizi gösterir.
```cpp
// Bu yaklaşımın bellek kullanımını azaltabileceğini ancak hızı düşürebileceğini unutmayın
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_TempFolder(u"C:\\TempFolder\\");

// Dizinin mevcut olduğundan emin olun ve yükleyin
System::IO::Directory::CreateDirectory_(loadOptions->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);
```


Bir belgeyi yüklerken belleğin yerine sabit sürücüyü nasıl kullanacağınızı gösterir.
```cpp
// Bir belgeyi yüklediğimizde, kaydetme işlemi gerçekleşirken çeşitli öğeler geçici olarak bellekte saklanır.
// Bunun yerine yerel dosya sisteminde geçici bir klasör kullanmak için bu seçeneği kullanabiliriz,
// bu, uygulamamızın bellek yükünü azaltacaktır.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// Belirtilen geçici klasör, yükleme işlemi öncesinde yerel dosya sisteminde mevcut olmalıdır.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", options);

// Klasör, yükleme işleminden kalan içerik olmadan kalıcı olacaktır.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Ayrıca Bakınız

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
