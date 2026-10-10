---
title: "Aspose::Words::PlainTextDocument::PlainTextDocument yapıcı"
linktitle: "PlainTextDocument"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PlainTextDocument::PlainTextDocument yapıcı. Bir akıştan düz metin belgesi oluşturur. C++'ta dosya formatını otomatik olarak algılar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Bir akıştan düz metin belgesi oluşturur. Dosya biçimini otomatik olarak algılar.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Metnin çıkarılacağı akış. |
## Açıklamalar


Belge akışın başında depolanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

## Örnekler



Akış kullanarak bir Microsoft Word belgesinin içeriğini düz metin olarak nasıl yükleyeceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStream.docx");

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStream.docx", System::IO::FileMode::Open);
    auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(stream);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```

## Ayrıca Bakınız

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Bir akıştan düz metin belgesi oluşturur. Şifreleme parolası gibi ek seçenekleri belirtmeye olanak tanır.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Metnin çıkarılacağı akış. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Bir belgeyi yüklerken kullanılacak ek seçenekler. **null** olabilir. |
## Açıklamalar


Belge akışın başında depolanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

## Örnekler



Akış kullanarak şifreli bir Microsoft Word belgesinin içeriğini düz metin olarak nasıl yükleyeceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Password(u"MyPassword");

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStreamWithOptions.docx", System::IO::FileMode::Open);
    auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(stream, loadOptions);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```

## Ayrıca Bakınız

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String\&) constructor


Bir dosyadan düz metin belgesi oluşturur. Dosya biçimini otomatik olarak algılar.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Metnin çıkarılacağı dosyanın adı. |

## Örnekler



Bir Microsoft Word belgesinin içeriğini düz metin olarak yüklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Ayrıca Bakınız

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Bir dosyadan düz metin belgesi oluşturur. Şifreleme parolası gibi ek seçenekleri belirtmeye olanak tanır.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Metnin çıkarılacağı dosyanın adı. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Bir belgeyi yüklerken kullanılacak ek seçenekler. **null** olabilir. |

## Örnekler



Şifreli bir Microsoft Word belgesinin içeriğini düz metin olarak nasıl yükleyeceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadEncrypted.docx", saveOptions);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Password(u"MyPassword");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.LoadEncrypted.docx", loadOptions);

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Ayrıca Bakınız

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream)
```

## Ayrıca Bakınız

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## Ayrıca Bakınız

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
