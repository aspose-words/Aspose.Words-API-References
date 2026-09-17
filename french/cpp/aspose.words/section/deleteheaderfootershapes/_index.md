---
title: "Aspose::Words::Section::DeleteHeaderFooterShapes méthode"
linktitle: "DeleteHeaderFooterShapes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Section::DeleteHeaderFooterShapes méthode. Supprime toutes les formes (objets de dessin) des en-têtes et pieds de page de cette section en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/section/deleteheaderfootershapes/
---
## Section::DeleteHeaderFooterShapes method


Supprime toutes les formes (objets de dessin) des en-têtes et pieds de page de cette section.

```cpp
void Aspose::Words::Section::DeleteHeaderFooterShapes()
```


## Exemples



Montre comment supprimer toutes les formes de tous les en-têtes et pieds de page d’une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un en-tête principal avec une forme.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);

// Créez un pied de page principal avec une image.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->InsertImage(get_ImageDir() + u"Logo icon.ico");

ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(1, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Supprimez toutes les formes des en-têtes et pieds de page de la première section.
doc->get_FirstSection()->DeleteHeaderFooterShapes();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Voir aussi

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
