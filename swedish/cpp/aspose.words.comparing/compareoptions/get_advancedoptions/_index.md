---
title: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions metod"
linktitle: "get_AdvancedOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions metod. Anger avancerade jämförelsealternativ som kan hjälpa till att producera mer exakt jämförelsesresultat i C++."
type: docs
weight: 2500
url: /sv/cpp/aspose.words.comparing/compareoptions/get_advancedoptions/
---
## CompareOptions::get_AdvancedOptions method


Anger avancerade jämförelsealternativ som kan hjälpa till att producera mer exakt jämförelsesresultat.

```cpp
const System::SharedPtr<Aspose::Words::Comparing::AdvancedCompareOptions> & Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions() const
```


## Exempel



Visar hur man jämför dokument utan att ta hänsyn till DML:s unika ID.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID original.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID compare.docx");

// Som standard ignorerar inte Aspose.Words DML:s unika ID, och antalet revisioner var 2.
// Om vi ignorerar DML:s unika ID, var antalet revisioner 0.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreDmlUniqueId(isIgnoreDmlUniqueId);

docA->Compare(docB, u"Aspose.Words", System::DateTime::get_Now(), compareOptions);

ASSERT_EQ(isIgnoreDmlUniqueId ? 0 : 2, docA->get_Revisions()->get_Count());
```

## Se även

* Class [AdvancedCompareOptions](../../advancedcompareoptions/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
