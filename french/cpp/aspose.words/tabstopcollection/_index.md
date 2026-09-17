---
title: "Aspose::Words::TabStopCollection classe"
linktitle: "TabStopCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TabStopCollection classe. Une collection d'objets TabStop qui représentent des tabulations personnalisées pour un paragraphe ou un style. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 69000
url: /fr/cpp/aspose.words/tabstopcollection/
---
## TabStopCollection class


Une collection d'objets [TabStop](../tabstop/) qui représentent des tabulations personnalisées pour un paragraphe ou un style. Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStopCollection : public Aspose::Words::InternableComplexAttr,
                          public Aspose::Words::IExpandableAttr
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Ajoute ou remplace une tabulation dans la collection. |
| [Add](./add/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Ajoute ou remplace une tabulation dans la collection. |
| [After](./after/)(double) | Obtient la première tabulation à droite de la position spécifiée. |
| [Before](./before/)(double) | Obtient la première tabulation à gauche de la position spécifiée. |
| [Clear](./clear/)() | Supprime toutes les positions de tabulation. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStopCollection\>\&) | Détermine si la [TabStopCollection](./) spécifiée est égale en valeur à la [TabStopCollection](./) actuelle. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [get_Count](./get_count/)() | Obtient le nombre de tabulations dans la collection. |
| [GetHashCode](./gethashcode/)() const override | Servit de fonction de hachage pour ce type. |
| [GetIndexByPosition](./getindexbyposition/)(double) | Obtient l'index d'une tabulation avec la position spécifiée en points. |
| [GetPositionByIndex](./getpositionbyindex/)(int32_t) | Obtient la position (en points) de la tabulation à l'index spécifié. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtient une tabulation à l'index donné. |
| [idx_get](./idx_get/)(double) | Obtient une tabulation à la position spécifiée. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveByIndex](./removebyindex/)(int32_t) | Supprime une tabulation à l'index spécifié de la collection. |
| [RemoveByPosition](./removebyposition/)(double) | Supprime une tabulation à la position spécifiée de la collection. |
| static [Type](./type/)() |  |
## Remarques


Dans les documents Microsoft Word, une tabulation peut être définie dans les propriétés d'un style de paragraphe ou directement dans les propriétés d'un paragraphe. Un style peut être basé sur un autre style. Par conséquent, l'ensemble complet des tabulations pour un objet donné est une combinaison des tabulations définies directement sur cet objet et des tabulations héritées des styles parents.

Dans Aspose.Words, lorsque vous obtenez une [TabStopCollection](./) pour un paragraphe ou un style, elle ne contient que les tabulations personnalisées définies directement pour ce paragraphe ou ce style. La collection n'inclut pas les tabulations définies dans les styles parents ou les tabulations par défaut.

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

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
