---
title: "Método Aspose::Words::Document::get_LastSection"
linktitle: "get_LastSection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::get_LastSection. Obtiene la última sección del documento en C++."
type: docs
weight: 35000
url: /es/cpp/aspose.words/document/get_lastsection/
---
## Document::get_LastSection method


Obtiene la última sección del documento.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_LastSection()
```


## Ejemplos



Muestra cómo crear una nueva sección con un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento en blanco contiene una sección por defecto,
// que contiene nodos hijos que podemos editar.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Utiliza un document builder para añadir texto a la primera sección.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Crea una segunda sección insertando un salto de sección.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Cada sección tiene su propia configuración de página.
// Podemos dividir el texto en la segunda sección en dos columnas.
// Esto no afectará al texto en la primera sección.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```

## Ver también

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
