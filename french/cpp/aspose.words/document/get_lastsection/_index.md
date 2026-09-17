---
title: "Aspose::Words::Document::get_LastSection méthode"
linktitle: "get_LastSection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_LastSection méthode. Obtient la dernière section du document en C++."
type: docs
weight: 35000
url: /fr/cpp/aspose.words/document/get_lastsection/
---
## Document::get_LastSection method


Obtient la dernière section du document.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_LastSection()
```


## Exemples



Montre comment créer une nouvelle section avec un constructeur de document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un document vierge contient une section par défaut,
// qui contient des nœuds enfants que nous pouvons modifier.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Utilisez un constructeur de document pour ajouter du texte à la première section.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Créez une deuxième section en insérant un saut de section.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Chaque section possède ses propres paramètres de mise en page.
// Nous pouvons diviser le texte de la deuxième section en deux colonnes.
// Cela n'affectera pas le texte de la première section.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```

## Voir aussi

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
