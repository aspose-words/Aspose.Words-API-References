---
title: "Aspose::Words::Tables::Table::Table constructor"
linktitle: "Table"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Table::Table constructor. Inicializa una nueva instancia de la clase Table en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.tables/table/table/
---
## Table::Table constructor


Inicializa una nueva instancia de la clase [Table](../).

```cpp
Aspose::Words::Tables::Table::Table(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento propietario. |
## Observaciones


Cuando se crea [Table](../), pertenece al documento especificado, pero aún no forma parte del documento y [ParentNode](../../../aspose.words/node/get_parentnode/) es **null**.

Para agregar [Table](../) al documento utilice [InsertAfter1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) en la historia donde desea que la tabla sea insertada.

## Ejemplos



Muestra cómo crear una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Las tablas contienen filas, que contienen celdas, que pueden tener párrafos
// con elementos típicos como segmentos, formas y incluso otras tablas.
// Llamar al método "EnsureMinimum" en una tabla garantizará que
// la tabla tenga al menos una fila, una celda y un párrafo.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Agrega texto a la primera celda de la primera fila de la tabla.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```

## Ver también

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
