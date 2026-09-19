---
title: "Aspose::Words::Section::DeleteHeaderFooterShapes metodo"
linktitle: "DeleteHeaderFooterShapes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Section::DeleteHeaderFooterShapes metodo. Elimina tutte le forme (oggetti di disegno) dalle intestazioni e dai piè di pagina di questa sezione in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/section/deleteheaderfootershapes/
---
## Section::DeleteHeaderFooterShapes method


Elimina tutte le forme (oggetti di disegno) dalle intestazioni e dai piè di pagina di questa sezione.

```cpp
void Aspose::Words::Section::DeleteHeaderFooterShapes()
```


## Esempi



Mostra come rimuovere tutte le forme da tutte le intestazioni e i piè di pagina in una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un'intestazione primaria con una forma.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);

// Crea un piè di pagina primario con un'immagine.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->InsertImage(get_ImageDir() + u"Logo icon.ico");

ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Rimuovi tutte le forme dalle intestazioni e dai piè di pagina nella prima sezione.
doc->get_FirstSection()->DeleteHeaderFooterShapes();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Vedi anche

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
