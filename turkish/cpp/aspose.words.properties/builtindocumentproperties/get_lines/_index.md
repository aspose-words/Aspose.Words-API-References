---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines metodu"
linktitle: "get_Lines"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines metodu. Belgedeki satır sayısının tahmini bir değerini C++'ta temsil eder."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_lines/
---
## BuiltInDocumentProperties::get_Lines method


Belgedeki satır sayısının tahmini bir değerini temsil eder.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines()
```

## Açıklamalar


Aspose.Words bu özelliği, [UpdateWordCount()](../../../aspose.words/document/updatewordcount/) çağırdığınızda günceller.

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

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
