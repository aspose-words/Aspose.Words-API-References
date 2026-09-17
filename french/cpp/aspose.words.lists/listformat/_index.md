---
title: "classe Aspose::Words::Lists::ListFormat"
linktitle: "ListFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Lists::ListFormat. Permet de contrôler le format de liste appliqué à un paragraphe. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.lists/listformat/
---
## ListFormat class


Permet de contrôler le formatage de liste appliqué à un paragraphe. Pour en savoir plus, consultez l’article de documentation [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListFormat : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ApplyBulletDefault](./applybulletdefault/)() | Démarre une nouvelle liste à puces par défaut et l'applique au paragraphe. |
| [ApplyNumberDefault](./applynumberdefault/)() | Démarre une nouvelle liste numérotée par défaut et l'applique au paragraphe. |
| [get_IsListItem](./get_islistitem/)() | Vrai lorsque le paragraphe a un format de puces ou de numérotation appliqué. |
| [get_List](./get_list/)() | Obtient ou définit la liste dont ce paragraphe fait partie. |
| [get_ListLevel](./get_listlevel/)() | Renvoie le formatage du niveau de liste ainsi que les éventuelles surcharges de formatage appliquées au paragraphe actuel. |
| [get_ListLevelNumber](./get_listlevelnumber/)() | Obtient ou définit le numéro du niveau de liste (0 à 8) pour le paragraphe. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ListIndent](./listindent/)() | Augmente le niveau de liste du paragraphe actuel d'un niveau. |
| [ListOutdent](./listoutdent/)() | Diminue le niveau de liste du paragraphe actuel d'un niveau. |
| [RemoveNumbers](./removenumbers/)() | Supprime les numéros ou puces du paragraphe actuel et définit le niveau de liste à zéro. |
| [set_List](./set_list/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Définisseur pour [Aspose::Words::Lists::ListFormat::get_List](./get_list/). |
| [set_ListLevelNumber](./set_listlevelnumber/)(int32_t) | Définisseur pour [Aspose::Words::Lists::ListFormat::get_ListLevelNumber](./get_listlevelnumber/). |
| static [Type](./type/)() |  |
## Remarques


Un paragraphe dans un document Microsoft Word peut être à puces ou numéroté. Lorsqu'un paragraphe est à puces ou numéroté, on dit qu'un formatage de liste est appliqué au paragraphe.

Vous ne créez pas d'objets de la classe [ListFormat](./) directement. Vous accédez à [ListFormat](./) en tant que propriété d'un autre objet pouvant avoir un formatage de liste associé. Pour le moment, les objets pouvant avoir un formatage de liste sont : [Paragraph](../../aspose.words/paragraph/), [Style](../../aspose.words/style/) et [DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

Le formatage de liste lui‑même est stocké dans un objet [List](../list/) qui est enregistré séparément des paragraphes. Les objets de liste sont stockés dans une collection [ListCollection](../listcollection/). Il existe une seule collection [ListCollection](../listcollection/) par [Document](../../aspose.words/document/).

Les paragraphes n'appartiennent pas physiquement à une liste. Les paragraphes font simplement référence à un objet de liste particulier via la propriété [List](./get_list/) et à un niveau particulier de la liste via la propriété [ListLevelNumber](./get_listlevelnumber/). En définissant ces deux propriétés, vous contrôlez les puces et la numérotation appliquées à un paragraphe.

## Exemples



Montre comment travailler avec les niveaux de listes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Voici deux types de listes que nous pouvons créer à l'aide d'un constructeur de document.
// 1 -  Une liste numérotée :
// Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// En définissant la propriété "ListLevelNumber", nous pouvons augmenter le niveau de la liste
// pour commencer une sous‑liste autonome à l'élément de liste actuel.
// Le modèle de liste Microsoft Word appelé "NumberDefault" utilise des chiffres pour créer des niveaux de liste pour le premier niveau de liste.
// Les niveaux de liste plus profonds utilisent des lettres et des chiffres romains minuscules.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Une liste à puces :
// Cette liste appliquera une indentation et un symbole de puce ("•") avant chaque paragraphe.
// Les niveaux plus profonds de cette liste utiliseront des symboles différents, tels que "■" et "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Nous pouvons désactiver le formatage de liste pour ne pas formater les paragraphes suivants comme des listes en désactivant le drapeau "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
