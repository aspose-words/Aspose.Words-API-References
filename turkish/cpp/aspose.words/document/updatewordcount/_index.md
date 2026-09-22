---
title: "Aspose::Words::Document::UpdateWordCount yöntemi"
linktitle: "UpdateWordCount"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::UpdateWordCount yöntemi. C++'ta belgenin kelime sayısı özelliklerini günceller."
type: docs
weight: 101000
url: /tr/cpp/aspose.words/document/updatewordcount/
---
## Document::UpdateWordCount() method


Belgenin kelime sayısı özelliklerini günceller.

```cpp
void Aspose::Words::Document::UpdateWordCount()
```

## Açıklamalar


[UpdateWordCount](./) recalculates and updates Characters, [Words](../../) and Paragraphs properties in the [BuiltInDocumentProperties](../get_builtindocumentproperties/) collection of the [Document](../).

Şunu unutmayın ki [UpdateWordCount](./) satır ve sayfa sayısı özelliklerini güncellemez. Bunu yapmak için [UpdateWordCount](./) aşırı yüklemesini kullanın ve **true** değerini parametre olarak geçirin.

Değerlendirme sürümünü kullandığınızda, değerlendirme filigranı da kelime sayısına dahil edilir.

## Örnekler



Bir belgede tüm liste etiketlerini nasıl güncelleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words bu tür belge ölçümlerini gerçek zamanlı olarak izlemez.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// Bu özelliklerden üçünün doğru değerlerini elde etmek için onları manuel olarak güncellememiz gerekir.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// Satır sayısı için, güncelleme yönteminin belirli bir aşırı yüklemesini çağırmamız gerekir.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateWordCount(bool) method


Belgenin kelime sayısı özelliklerini günceller, isteğe bağlı olarak [Lines](../../../aspose.words.properties/builtindocumentproperties/get_lines/) özelliğini de günceller.

```cpp
void Aspose::Words::Document::UpdateWordCount(bool updateLinesCount)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| updateLinesCount | bool | Belgedeki satır sayısının hesaplanması isteniyorsa **true**. |

## Örnekler



Bir belgede tüm liste etiketlerini nasıl güncelleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->Write(System::String(u"Ut enim ad minim veniam, ") + u"quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words bu tür belge ölçümlerini gerçek zamanlı olarak izlemez.
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(0, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Paragraphs());
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

// Bu özelliklerden üçünün doğru değerlerini elde etmek için onları manuel olarak güncellememiz gerekir.
doc->UpdateWordCount();

ASSERT_EQ(196, doc->get_BuiltInDocumentProperties()->get_Characters());
ASSERT_EQ(36, doc->get_BuiltInDocumentProperties()->get_Words());
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Paragraphs());

// Satır sayısı için, güncelleme yönteminin belirli bir aşırı yüklemesini çağırmamız gerekir.
ASSERT_EQ(1, doc->get_BuiltInDocumentProperties()->get_Lines());

doc->UpdateWordCount(true);

ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Lines());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
