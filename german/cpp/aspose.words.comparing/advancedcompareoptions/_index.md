---
title: "Aspose::Words::Comparing::AdvancedCompareOptions Klasse"
linktitle: "AdvancedCompareOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comparing::AdvancedCompareOptions Klasse. Ermöglicht das Festlegen erweiterter Vergleichsoptionen in C++."
type: docs
weight: 500
url: /de/cpp/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class


Ermöglicht das Festlegen erweiterter Vergleichsoptionen.

```cpp
class AdvancedCompareOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [AdvancedCompareOptions](./advancedcompareoptions/)() |  |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() const | Gibt an, ob Unterschiede in der eindeutigen DrawingML‑Id ignoriert werden sollen. |
| [get_IgnoreStoreItemId](./get_ignorestoreitemid/)() const | Gibt an, ob Unterschiede in der Store‑Item‑Id des StructuredDocumentTag ignoriert werden sollen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Setter für [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreStoreItemId](./set_ignorestoreitemid/)(bool) | Setter für [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId](./get_ignorestoreitemid/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man SDT mit gleichem Inhalt, aber unterschiedlicher Store‑Item‑Id vergleicht.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Konfigurieren Sie Optionen, um SDT mit gleichem Inhalt, aber unterschiedlicher Store‑Item‑Id zu vergleichen.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## Siehe auch

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
