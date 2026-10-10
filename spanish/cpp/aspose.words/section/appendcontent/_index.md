---
title: "Aspose::Words::Section::AppendContent método"
linktitle: "AppendContent"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Section::AppendContent método. Inserta una copia del contenido de la sección origen al final de esta sección en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/section/appendcontent/
---
## Section::AppendContent method


Inserta una copia del contenido de la sección origen al final de esta sección.

```cpp
void Aspose::Words::Section::AppendContent(const System::SharedPtr<Aspose::Words::Section> &sourceSection)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceSection | const System::SharedPtr\<Aspose::Words::Section\>\& | La sección de la cual copiar el contenido. |
## Observaciones


Solo se copia el contenido del [Body](../get_body/) de la sección origen; la configuración de página, encabezados y pies de página no se copian.

Los nodos se importan automáticamente si la sección de origen pertenece a un documento diferente.

No se crea una nueva sección en el documento de destino.

## Ejemplos



Muestra cómo anexar el contenido de una sección a otra sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

System::SharedPtr<Aspose::Words::Section> section = doc->get_Sections()->idx_get(2);

ASSERT_EQ(System::String(u"Section 3") + Aspose::Words::ControlChar::SectionBreak(), section->GetText());

// Inserta el contenido de la primera sección al comienzo de la tercera sección.
System::SharedPtr<Aspose::Words::Section> sectionToPrepend = doc->get_Sections()->idx_get(0);
section->PrependContent(sectionToPrepend);

// Inserta el contenido de la segunda sección al final de la tercera sección.
System::SharedPtr<Aspose::Words::Section> sectionToAppend = doc->get_Sections()->idx_get(1);
section->AppendContent(sectionToAppend);

// Los métodos \"PrependContent\" y \"AppendContent\" no crearon ninguna sección nueva.
ASSERT_EQ(3, doc->get_Sections()->get_Count());
ASSERT_EQ(System::String(u"Section 1") + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 3" + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 2" + Aspose::Words::ControlChar::SectionBreak(), section->GetText());
```

## Ver también

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
