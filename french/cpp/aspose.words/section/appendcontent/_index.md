---
title: "Aspose::Words::Section::AppendContent méthode"
linktitle: "AppendContent"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Section::AppendContent méthode. Insère une copie du contenu de la section source à la fin de cette section en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/section/appendcontent/
---
## Section::AppendContent method


Insère une copie du contenu de la section source à la fin de cette section.

```cpp
void Aspose::Words::Section::AppendContent(const System::SharedPtr<Aspose::Words::Section> &sourceSection)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| sourceSection | const System::SharedPtr\<Aspose::Words::Section\>\& | La section dont le contenu doit être copié. |
## Remarques


Seul le contenu de [Body](../get_body/) de la section source est copié, la mise en page, les en-têtes et les pieds de page ne le sont pas.

Les nœuds sont automatiquement importés si la section source appartient à un document différent.

Aucune nouvelle section n'est créée dans le document de destination.

## Exemples



Montre comment ajouter le contenu d'une section à une autre section.
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

// Insérez le contenu de la première section au début de la troisième section.
System::SharedPtr<Aspose::Words::Section> sectionToPrepend = doc->get_Sections()->idx_get(0);
section->PrependContent(sectionToPrepend);

// Insérez le contenu de la deuxième section à la fin de la troisième section.
System::SharedPtr<Aspose::Words::Section> sectionToAppend = doc->get_Sections()->idx_get(1);
section->AppendContent(sectionToAppend);

// Les méthodes "PrependContent" et "AppendContent" n'ont pas créé de nouvelles sections.
ASSERT_EQ(3, doc->get_Sections()->get_Count());
ASSERT_EQ(System::String(u"Section 1") + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 3" + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 2" + Aspose::Words::ControlChar::SectionBreak(), section->GetText());
```

## Voir aussi

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
