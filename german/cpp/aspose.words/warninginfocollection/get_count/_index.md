---
title: "Aspose::Words::WarningInfoCollection::get_Count Methode"
linktitle: "get_Count"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::WarningInfoCollection::get_Count Methode. Gibt die Anzahl der im Sammlung enthaltenen Elemente in C++ zurück."
type: docs
weight: 8000
url: /de/cpp/aspose.words/warninginfocollection/get_count/
---
## WarningInfoCollection::get_Count method


Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück.

```cpp
int32_t Aspose::Words::WarningInfoCollection::get_Count()
```


## Beispiele



Zeigt, wie man Warnungen zu nicht unterstützten Formaten erhält.
```cpp
auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_WarningCallback(warnings);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"FB2 document.fb2", loadOptions);

ASSERT_EQ(u"The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings->idx_get(0)->get_Description());
ASSERT_EQ(1, warnings->get_Count());
```

## Siehe auch

* Class [WarningInfoCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
