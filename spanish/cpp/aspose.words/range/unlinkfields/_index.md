---
title: "Aspose::Words::Range::UnlinkFields método"
linktitle: "UnlinkFields"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Range::UnlinkFields. Desvincula campos en este rango en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words/range/unlinkfields/
---
## Range::UnlinkFields method


Desvincula los campos en este rango.

```cpp
void Aspose::Words::Range::UnlinkFields()
```

## Observaciones


Reemplaza todos los campos en este rango con sus resultados más recientes.

Para desvincular campos en todo el documento use [UnlinkFields](./).

## Ejemplos



Muestra cómo desvincular todos los campos en un rango.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

auto newSection = System::ExplicitCast<Aspose::Words::Section>(System::ExplicitCast<Aspose::Words::Node>(doc->get_Sections()->idx_get(0))->Clone(true));
doc->get_Sections()->Add(newSection);

doc->get_Sections()->idx_get(1)->get_Range()->UnlinkFields();
```

## Ver también

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
