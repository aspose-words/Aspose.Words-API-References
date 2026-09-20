---
title: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit método"
linktitle: "get_MeasureUnit"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit método. Permite especificar unidades de medida para aplicar al contenido del documento. El valor predeterminado es Centimeters en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/odtsaveoptions/get_measureunit/
---
## OdtSaveOptions::get_MeasureUnit method


Permite especificar unidades de medida para aplicar al contenido del documento. El valor predeterminado es [Centimeters](../../odtsavemeasureunit/)

```cpp
Aspose::Words::Saving::OdtSaveMeasureUnit Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit() const
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

* Enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
