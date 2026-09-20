---
title: "Aspose::Words::TextColumnCollection::idx_get método"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TextColumnCollection::idx_get método. Devuelve una columna de texto en el índice especificado en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/textcolumncollection/idx_get/
---
## TextColumnCollection::idx_get method


Devuelve una columna de texto en el índice especificado.

```cpp
System::SharedPtr<Aspose::Words::TextColumn> Aspose::Words::TextColumnCollection::idx_get(int32_t index)
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

* Class [TextColumn](../../textcolumn/)
* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
