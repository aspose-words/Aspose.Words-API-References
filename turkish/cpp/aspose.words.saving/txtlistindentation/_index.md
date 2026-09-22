---
title: "Aspose::Words::Saving::TxtListIndentation sınıfı"
linktitle: "TxtListIndentation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::TxtListIndentation sınıfı. Belge Text formatına dışa aktarılırken liste seviyelerinin nasıl girintilendiğini belirtir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 32000
url: /tr/cpp/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class


Belgenin [Text](../../aspose.words/saveformat/) formatına dışa aktarılırken liste seviyelerinin nasıl girintilendiğini belirtir. Daha fazla bilgi için [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) belge makalesini ziyaret edin.

```cpp
class TxtListIndentation : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Character](./get_character/)() const | Liste seviyelerini girintilemek için kullanılacak karakteri alır veya ayarlar. Varsayılan değer "\\0" olup, girinti olmadığını gösterir. |
| [get_Count](./get_count/)() const | Bir liste seviyesi başına girinti olarak kullanılacak [Character](./get_character/) sayısını alır veya ayarlar. Varsayılan değer 0'dır, bu da girinti olmadığını gösterir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Character](./set_character/)(char16_t) | [Aspose::Words::Saving::TxtListIndentation::get_Character](./get_character/) için ayarlayıcı. |
| [set_Count](./set_count/)(int32_t) | [Aspose::Words::Saving::TxtListIndentation::get_Count](./get_count/) için ayarlayıcı. |
| [TxtListIndentation](./txtlistindentation/)() |  |
| static [Type](./type/)() |  |

## Örnekler



Bir belgeyi düz metin olarak kaydederken liste girintisinin nasıl yapılandırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Üç seviyeli girintili bir liste oluşturun.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// Bir "TxtSaveOptions" nesnesi oluşturun, bunu belgenin "Save" yöntemine aktarabiliriz
// belgeyi düz metne kaydetme şeklini değiştirmek için.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// "Character" özelliğini kullanmak için bir karakter atamak üzere ayarlayın
// düz metinde liste girintisini taklit eden doldurma için.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// "Count" özelliğini kaç kez kullanılacağını belirtmek için ayarlayın
// her liste girinti seviyesi için doldurma karakterini yerleştirmek amacıyla.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
