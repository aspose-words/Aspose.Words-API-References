---
title: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 método"
linktitle: "get_IsStrictSchema11"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 método. Especifica si la exportación debe ajustarse estrictamente a la especificación ODT 1.1. OOo 3.0 muestra los archivos correctamente cuando contienen elementos y atributos de ODT 1.2. Use \"false\" para este propósito, o \"true\" para una conformidad estricta con la especificación 1.1. El valor predeterminado es false en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/odtsaveoptions/get_isstrictschema11/
---
## OdtSaveOptions::get_IsStrictSchema11 method


Especifica si la exportación debe ajustarse estrictamente a la especificación ODT 1.1. OOo 3.0 muestra los archivos correctamente cuando contienen elementos y atributos de ODT 1.2. Use "false" para este propósito, o "true" para una conformidad estricta con la especificación 1.1. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11() const
```


## Ejemplos



Muestra cómo hacer que un documento guardado cumpla con un esquema ODT más antiguo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Ver también

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
