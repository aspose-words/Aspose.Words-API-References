---
title: "Aspose::Words::TextColumnCollection::get_EvenlySpaced método"
linktitle: "get_EvenlySpaced"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TextColumnCollection::get_EvenlySpaced método. Verdadero si las columnas de texto tienen el mismo ancho y están espaciadas uniformemente en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/textcolumncollection/get_evenlyspaced/
---
## TextColumnCollection::get_EvenlySpaced method


Verdadero si las columnas de texto tienen igual ancho y están espaciadas uniformemente.

```cpp
bool Aspose::Words::TextColumnCollection::get_EvenlySpaced()
```


## Ejemplos



Muestra cómo crear columnas con espaciado desigual.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Determine la cantidad de espacio que tenemos disponible para organizar columnas.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// Establezca la primera columna como estrecha.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// Establezca la segunda columna para que ocupe el resto del espacio disponible dentro de los márgenes de la página.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## Ver también

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
