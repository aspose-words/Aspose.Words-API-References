---
title: "Aspose::Words::Comparing::AdvancedCompareOptions class"
linktitle: "AdvancedCompareOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions class. Consente di impostare opzioni avanzate di confronto in C++."
type: docs
weight: 500
url: /it/cpp/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class


Consente di impostare opzioni di confronto avanzate.

```cpp
class AdvancedCompareOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [AdvancedCompareOptions](./advancedcompareoptions/)() |  |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() const | Specifica se ignorare le differenze nell'Id univoco di DrawingML. |
| [get_IgnoreStoreItemId](./get_ignorestoreitemid/)() const | Specifica se ignorare le differenze nell'Id dell'elemento di archiviazione StructuredDocumentTag. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Setter per [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreStoreItemId](./set_ignorestoreitemid/)(bool) | Setter per [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId](./get_ignorestoreitemid/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come confrontare SDT con lo stesso contenuto ma con un id dell'elemento di archiviazione diverso.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Configura le opzioni per confrontare SDT con lo stesso contenuto ma con un id dell'elemento di archiviazione diverso.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## Vedi anche

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
