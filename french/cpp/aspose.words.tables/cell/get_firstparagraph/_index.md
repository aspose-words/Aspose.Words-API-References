---
title: "Aspose::Words::Tables::Cell::get_FirstParagraph méthode"
linktitle: "get_FirstParagraph"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Cell::get_FirstParagraph méthode. Obtient le premier paragraphe parmi les enfants immédiats en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.tables/cell/get_firstparagraph/
---
## Cell::get_FirstParagraph method


Obtient le premier paragraphe parmi les enfants immédiats.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Tables::Cell::get_FirstParagraph()
```


## Exemples



Montre comment créer une table imbriquée à l'aide d'un constructeur de document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Construisez la table externe.
System::SharedPtr<Aspose::Words::Tables::Cell> cell = builder->InsertCell();
builder->Writeln(u"Outer Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Outer Table Cell 2");
builder->EndTable();

// Déplacez-vous vers la première cellule de la table externe, puis construisez une autre table à l'intérieur de la cellule.
builder->MoveTo(cell->get_FirstParagraph());
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 2");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertNestedTable.docx");
```

## Voir aussi

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
