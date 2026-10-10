---
title: "Método Aspose::Words::PageSetup::get_Bidi"
linktitle: "get_Bidi"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PageSetup::get_Bidi. Especifica que esta sección contiene texto bidireccional (scripts complejos) en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/pagesetup/get_bidi/
---
## PageSetup::get_Bidi method


Especifica que esta sección contiene texto bidireccional (scripts complejos).

```cpp
bool Aspose::Words::PageSetup::get_Bidi()
```

## Observaciones


Cuando **true**, las columnas en esta sección se disponen de derecha a izquierda.

## Ejemplos



Muestra cómo establecer el orden de las columnas de texto en una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_TextColumns()->SetCount(3);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 3.");

// Establezca la propiedad "Bidi" a "true" para organizar las columnas comenzando desde el lado derecho de la página.
// El orden de las columnas coincidirá con la dirección del texto de derecha a izquierda.
// Establezca la propiedad "Bidi" a "false" para organizar las columnas comenzando desde el lado izquierdo de la página.
// El orden de las columnas coincidirá con la dirección del texto de izquierda a derecha.
pageSetup->set_Bidi(reverseColumns);

doc->Save(get_ArtifactsDir() + u"PageSetup.Bidi.docx");
```

## Ver también

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
