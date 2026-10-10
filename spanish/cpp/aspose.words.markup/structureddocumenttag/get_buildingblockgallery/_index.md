---
title: "Método Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery"
linktitle: "get_BuildingBlockGallery"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery. Especifica el tipo de bloque de construcción para este **SDT**. No puede ser nulo en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.markup/structureddocumenttag/get_buildingblockgallery/
---
## StructuredDocumentTag::get_BuildingBlockGallery method


Especifica el tipo de bloque de construcción para este **SDT**. No puede ser **null**.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery()
```

## Observaciones


Acceder a esta propiedad solo funcionará para los tipos de **SDT** [BuildingBlockGallery](../../sdttype/) y [DocPartObj](../../sdttype/). Es de solo lectura para los **SDT** del tipo parte de documento.

Para todos los demás tipos de SDT se producirá una excepción.

## Ejemplos



Muestra cómo insertar una etiqueta de documento estructurado como un bloque de construcción y establecer su categoría y galería.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto buildingBlockSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::BuildingBlockGallery, Aspose::Words::Markup::MarkupLevel::Block);
buildingBlockSdt->set_BuildingBlockCategory(u"Built-in");
buildingBlockSdt->set_BuildingBlockGallery(u"Table of Contents");

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(buildingBlockSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.BuildingBlockCategories.docx");
```

## Ver también

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
