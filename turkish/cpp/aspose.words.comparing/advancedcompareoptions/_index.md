---
title: "Aspose::Words::Comparing::AdvancedCompareOptions class"
linktitle: "AdvancedCompareOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comparing::AdvancedCompareOptions sınıfı. C++'da gelişmiş karşılaştırma seçeneklerini ayarlamayı sağlar."
type: docs
weight: 500
url: /tr/cpp/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class


Gelişmiş karşılaştırma seçeneklerini ayarlamaya izin verir.

```cpp
class AdvancedCompareOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [AdvancedCompareOptions](./advancedcompareoptions/)() |  |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() const | DrawingML benzersiz kimliğindeki farkı göz ardı edip etmeyeceğini belirtir. |
| [get_IgnoreStoreItemId](./get_ignorestoreitemid/)() const | StructuredDocumentTag depolama öğesi kimliğindeki farkı göz ardı edip etmeyeceğini belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/) için ayarlayıcı. |
| [set_IgnoreStoreItemId](./set_ignorestoreitemid/)(bool) | [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId](./get_ignorestoreitemid/) için ayarlayıcı. |
| static [Type](./type/)() |  |

## Örnekler



Aynı içeriğe sahip ancak farklı depolama öğesi kimliğine sahip SDT'yi nasıl karşılaştıracağınızı gösterir.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Aynı içeriğe sahip ancak farklı depolama öğesi kimliğine sahip SDT'yi karşılaştırmak için seçenekleri yapılandırın.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
