---
title: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData method"
linktitle: "get_IgnoreOleData"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData method. Especifica si se debe ignorar los datos OLE en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.loading/loadoptions/get_ignoreoledata/
---
## LoadOptions::get_IgnoreOleData method


Especifica si se deben ignorar los datos OLE.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_IgnoreOleData() const
```

## Observaciones


Ignorar los datos OLE puede reducir el consumo de memoria y aumentar el rendimiento sin pérdida de datos en caso de que el formato de destino no admita objetos OLE.

El valor predeterminado es **false**.

## Ejemplos



Muestra cómo ignorar los datos OLE durante la carga.
```cpp
// Ignorar los datos OLE puede reducir el consumo de memoria y aumentar el rendimiento
// sin pérdida de datos en caso de que el formato de destino no admita objetos OLE.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_IgnoreOleData(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE objects.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.IgnoreOleData.docx");
```

## Ver también

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
