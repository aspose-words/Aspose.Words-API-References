---
title: "Aspose::Words::Section::DeleteHeaderFooterShapes Methode"
linktitle: "DeleteHeaderFooterShapes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Section::DeleteHeaderFooterShapes Methode. Löscht alle Formen (Zeichnungsobjekte) aus den Kopf- und Fußzeilen dieses Abschnitts in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words/section/deleteheaderfootershapes/
---
## Section::DeleteHeaderFooterShapes method


Löscht alle Formen (Zeichnungsobjekte) aus den Kopf- und Fußzeilen dieses Abschnitts.

```cpp
void Aspose::Words::Section::DeleteHeaderFooterShapes()
```


## Beispiele



Zeigt, wie man alle Formen aus allen Kopf‑ und Fußzeilen in einem Abschnitt entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie eine primäre Kopfzeile mit einer Form.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);

// Erstellen Sie eine primäre Fußzeile mit einem Bild.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->InsertImage(get_ImageDir() + u"Logo icon.ico");

ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Entfernen Sie alle Formen aus den Kopf- und Fußzeilen im ersten Abschnitt.
doc->get_FirstSection()->DeleteHeaderFooterShapes();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Siehe auch

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
