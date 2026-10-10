---
title: "Aspose::Words::Comparing::AdvancedCompareOptions klass"
linktitle: "AdvancedCompareOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comparing::AdvancedCompareOptions klass. Tillåter att ställa in avancerade jämförelsealternativ i C++."
type: docs
weight: 500
url: /sv/cpp/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class


Tillåter att ställa in avancerade jämförelsealternativ.

```cpp
class AdvancedCompareOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [AdvancedCompareOptions](./advancedcompareoptions/)() |  |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() const | Anger om skillnad i DrawingML unika Id ska ignoreras. |
| [get_IgnoreStoreItemId](./get_ignorestoreitemid/)() const | Anger om skillnad i StructuredDocumentTag lagringsobjektets Id ska ignoreras. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Sättare för [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreStoreItemId](./set_ignorestoreitemid/)(bool) | Sättare för [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId](./get_ignorestoreitemid/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man jämför SDT med samma innehåll men olika lagringsobjekt-id.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Konfigurera alternativ för att jämföra SDT med samma innehåll men olika lagringsobjekt-id.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## Se även

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
