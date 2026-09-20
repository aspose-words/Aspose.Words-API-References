---
title: "Aspose::Words::PageVerticalAlignment enumeración"
linktitle: "PageVerticalAlignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageVerticalAlignment enumeración. Especifica la justificación vertical del texto en cada página en C++."
type: docs
weight: 108000
url: /es/cpp/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enum


Especifica la justificación vertical del texto en cada página.

```cpp
enum class PageVerticalAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Inferior | 3 | El texto está alineado en la parte inferior de la página. |
| Centro | 1 | El texto está alineado en el medio de la página. |
| Justificar | 2 | El texto se extiende para llenar la página. |
| Superior | 0 | El texto está alineado en la parte superior de la página. |


## Ejemplos



Muestra cómo aplicar y revertir la configuración de página en secciones de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifique las propiedades de configuración de página de la sección actual del generador y añada texto.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Si iniciamos una nueva sección usando un generador de documentos,
// heredará las propiedades de configuración de página actuales del generador.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Podemos revertir sus propiedades de configuración de página a sus valores predeterminados usando el método "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
