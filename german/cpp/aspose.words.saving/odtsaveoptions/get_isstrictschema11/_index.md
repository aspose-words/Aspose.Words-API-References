---
title: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 Methode"
linktitle: "get_IsStrictSchema11"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 Methode. Gibt an, ob der Export strikt der ODT‑Spezifikation 1.1 entsprechen soll. OOo 3.0 zeigt Dateien korrekt an, wenn sie Elemente und Attribute von ODT 1.2 enthalten. Verwenden Sie hierfür \"false\" oder \"true\" für die strikte Konformität zur Spezifikation 1.1. Der Standardwert ist in C++ false."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/odtsaveoptions/get_isstrictschema11/
---
## OdtSaveOptions::get_IsStrictSchema11 method


Gibt an, ob der Export strikt der ODT-Spezifikation 1.1 entsprechen soll. OOo 3.0 zeigt Dateien korrekt an, wenn sie Elemente und Attribute von ODT 1.2 enthalten. Verwenden Sie "false" für diesen Zweck oder "true" für strikte Konformität zur Spezifikation 1.1. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11() const
```


## Beispiele



Zeigt, wie ein gespeichertes Dokument an ein älteres ODT-Schema angepasst wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Siehe auch

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
