---
title: "Aspose::Words::TabStopCollection::After méthode"
linktitle: "After"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TabStopCollection::After méthode. Obtient le premier arrêt de tabulation à droite de la position spécifiée en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/tabstopcollection/after/
---
## TabStopCollection::After method


Obtient la première tabulation à droite de la position spécifiée.

```cpp
System::SharedPtr<Aspose::Words::TabStop> Aspose::Words::TabStopCollection::After(double position)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| position | double | La position de référence (en points). |

### ReturnValue

Un objet tab stop ou **null** si aucun tab stop approprié n'a été trouvé.
## Remarques


Ignore les tab stops avec [Alignment](../../tabstop/get_alignment/) défini sur [Bar](../../tabalignment/).

## Exemples



Montre comment travailler avec la collection de tabulations d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 points correspondent à un "pouce" sur la règle de tabulation de Microsoft Word.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Chaque caractère "tab" déplace le curseur du constructeur vers l'emplacement de la prochaine tabulation.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// Chaque paragraphe obtient sa collection de tabulations, qui clone ses valeurs à partir de la collection de tabulations du constructeur de document.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// Une collection de tabulations peut nous indiquer les TabStops avant et après certaines positions.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// Nous pouvons effacer la collection de tabulations d'un paragraphe pour revenir au comportement de tabulation par défaut.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## Voir aussi

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
