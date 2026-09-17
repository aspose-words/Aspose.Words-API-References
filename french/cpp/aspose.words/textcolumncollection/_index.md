---
title: "Aspose::Words::TextColumnCollection classe"
linktitle: "TextColumnCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TextColumnCollection classe. Une collection d’objets TextColumn qui représentent toutes les colonnes de texte dans une section d’un document. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 71000
url: /fr/cpp/aspose.words/textcolumncollection/
---
## TextColumnCollection class


Une collection d’objets [TextColumn](../textcolumn/) qui représentent toutes les colonnes de texte dans une section d’un document. Pour en savoir plus, consultez l’article de documentation [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumnCollection : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Count](./get_count/)() | Obtient le nombre de colonnes dans la section d’un document. |
| [get_EvenlySpaced](./get_evenlyspaced/)() | Vrai si les colonnes de texte ont une largeur égale et sont espacées uniformément. |
| [get_LineBetween](./get_linebetween/)() | Lorsque **true**, ajoute une ligne verticale entre les colonnes. |
| [get_Spacing](./get_spacing/)() | Lorsque les colonnes sont espacées uniformément, obtient ou définit la quantité d’espace entre chaque colonne en points. |
| [get_Width](./get_width/)() | Lorsque les colonnes sont espacées uniformément, obtient la largeur des colonnes. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Renvoie une colonne de texte à l’indice spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EvenlySpaced](./set_evenlyspaced/)(bool) | Mutateur pour [Aspose::Words::TextColumnCollection::get_EvenlySpaced](./get_evenlyspaced/). |
| [set_LineBetween](./set_linebetween/)(bool) | Mutateur pour [Aspose::Words::TextColumnCollection::get_LineBetween](./get_linebetween/). |
| [set_Spacing](./set_spacing/)(double) | Mutateur pour [Aspose::Words::TextColumnCollection::get_Spacing](./get_spacing/). |
| [SetCount](./setcount/)(int32_t) | Dispose le texte en le répartissant dans le nombre spécifié de colonnes de texte. |
| static [Type](./type/)() |  |
## Remarques


Utilisez [SetCount()](./setcount/) pour définir le nombre de colonnes de texte.

Pour que toutes les colonnes aient une largeur égale et soient espacées uniformément, définissez [EvenlySpaced](./get_evenlyspaced/) sur **true** et spécifiez la quantité d’espace entre les colonnes dans [Spacing](./get_spacing/). MS Word calculera automatiquement la largeur des colonnes.

Si vous avez [EvenlySpaced](./get_evenlyspaced/) défini sur **false**, vous devez spécifier la largeur et l’espacement pour chaque colonne individuellement. Utilisez l’indexeur pour accéder aux objets [TextColumn](../textcolumn/) individuels.

Lorsque vous utilisez des largeurs de colonne personnalisées, assurez‑vous que la somme de toutes les largeurs de colonne et des espacements entre elles soit égale à la largeur de la page moins les marges gauche et droite.

## Exemples



Montre comment créer plusieurs colonnes espacées uniformément dans une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
