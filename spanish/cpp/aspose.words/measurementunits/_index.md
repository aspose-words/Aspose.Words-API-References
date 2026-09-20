---
title: "Aspose::Words::MeasurementUnits enum"
linktitle: "MeasurementUnits"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::MeasurementUnits enum. Especifica la unidad de medida en C++."
type: docs
weight: 100000
url: /es/cpp/aspose.words/measurementunits/
---
## MeasurementUnits enum


Especifica la unidad de medida.

```cpp
enum class MeasurementUnits
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Pulgadas | 0 | Pulgadas. |
| Centímetros | 1 | Centímetros. |
| Milímetros | 2 | Milímetros. |
| Puntos | 3 | Puntos. |
| Picas | 4 | Picas (comúnmente usadas en el espaciado de fuentes de máquinas de escribir tradicionales). |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
