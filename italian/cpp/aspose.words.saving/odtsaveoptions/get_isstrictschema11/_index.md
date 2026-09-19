---
title: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 metodo"
linktitle: "get_IsStrictSchema11"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 method. Specifica se l'esportazione deve corrispondere strettamente alla specifica ODT 1.1. OOo 3.0 visualizza correttamente i file quando contengono elementi e attributi di ODT 1.2. Usa \"false\" a questo scopo, oppure \"true\" per una conformità rigorosa alla specifica 1.1. Il valore predefinito è false in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/odtsaveoptions/get_isstrictschema11/
---
## OdtSaveOptions::get_IsStrictSchema11 method


Specifica se l'esportazione deve corrispondere strettamente alla specifica ODT 1.1. OOo 3.0 visualizza correttamente i file quando contengono elementi e attributi di ODT 1.2. Usa "false" a questo scopo, o "true" per la conformità rigorosa alla specifica 1.1. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11() const
```


## Esempi



Mostra come far conformare un documento salvato a uno schema ODT più vecchio.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Vedi anche

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
