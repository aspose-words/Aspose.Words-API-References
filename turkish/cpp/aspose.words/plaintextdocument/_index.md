---
title: "Aspose::Words::PlainTextDocument class"
linktitle: "PlainTextDocument"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PlainTextDocument sınıfı. Belgenin içeriğinin düz metin temsilini çıkarmaya olanak tanır. Daha fazla bilgi edinmek için C++ belgeleri makalesini ziyaret edin."
type: docs
weight: 50000
url: /tr/cpp/aspose.words/plaintextdocument/
---
## PlainTextDocument class


Belgenin içeriğinin düz metin temsilini çıkarmaya izin verir. Daha fazla bilgi edinmek için, [Working with Text Document](https://docs.aspose.com/words/cpp/working-with-text-document/) dokümantasyon makalesini ziyaret edin.

```cpp
class PlainTextDocument : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Belgenin [BuiltInDocumentProperties](./get_builtindocumentproperties/) alır. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() const | Belgenin [CustomDocumentProperties](./get_customdocumentproperties/) alır. |
| [get_Text](./get_text/)() const | Belgenin metinsel içeriğini bir dize olarak birleştirir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&) | Bir dosyadan düz metin belgesi oluşturur. Dosya biçimini otomatik olarak algılar. |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Bir dosyadan düz metin belgesi oluşturur. Şifreleme parolası gibi ek seçenekleri belirtmeye olanak tanır. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&) | Bir akıştan düz metin belgesi oluşturur. Dosya biçimini otomatik olarak algılar. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Bir akıştan düz metin belgesi oluşturur. Şifreleme parolası gibi ek seçenekleri belirtmeye olanak tanır. |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&) |  |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
