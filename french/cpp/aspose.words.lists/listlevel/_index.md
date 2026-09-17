---
title: "Aspose::Words::Lists::ListLevel class"
linktitle: "ListLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::ListLevel class. Définit la mise en forme d’un niveau de liste. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.lists/listlevel/
---
## ListLevel class


Définit le formatage d’un niveau de liste. Pour en savoir plus, consultez l’article de documentation [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListLevel : public Aspose::Words::IRunAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [CreatePictureBullet](./createpicturebullet/)() | Crée une forme de puce image pour le niveau de liste actuel. |
| [DeletePictureBullet](./deletepicturebullet/)() | Supprime la puce image du niveau de liste actuel. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::ListLevel\>\&) | Compare avec le [ListLevel](./) spécifié. |
| [get_Alignment](./get_alignment/)() const | Obtient ou définit la justification du numéro réel de l'élément de liste. |
| [get_CustomNumberStyleFormat](./get_customnumberstyleformat/)() | Obtient ou définit le format de style de numéro personnalisé pour ce niveau de liste. Par exemple : "a, ç, ĝ, ...". |
| [get_Font](./get_font/)() | Spécifie le formatage des caractères utilisé pour l'étiquette de la liste. |
| [get_ImageData](./get_imagedata/)() | Renvoie les données d'image de la forme de puce image pour le niveau de liste actuel. |
| [get_IsLegal](./get_islegal/)() const | Vrai si le niveau convertit tous les numéros hérités en arabe, faux s'il préserve leur style de numéro. |
| [get_LinkedStyle](./get_linkedstyle/)() | Obtient ou définit le style de paragraphe lié à ce niveau de liste. |
| [get_NumberFormat](./get_numberformat/)() const | Renvoie ou définit le format de numéro pour le niveau de liste. |
| [get_NumberPosition](./get_numberposition/)() const | Renvoie ou définit la position (en points) du numéro ou de la puce pour le niveau de liste. |
| [get_NumberStyle](./get_numberstyle/)() const | Renvoie ou définit le style de numéro pour ce niveau de liste. |
| [get_RestartAfterLevel](./get_restartafterlevel/)() const | Définit ou renvoie le niveau de liste qui doit apparaître avant que le niveau de liste spécifié ne redémarre la numérotation. |
| [get_StartAt](./get_startat/)() | Renvoie ou définit le numéro de départ pour ce niveau de liste. |
| [get_TabPosition](./get_tabposition/)() const | Renvoie ou définit la position de tabulation (en points) pour le niveau de liste. |
| [get_TextPosition](./get_textposition/)() const | Renvoie ou définit la position (en points) de la deuxième ligne du texte enroulé pour le niveau de liste. |
| [get_TrailingCharacter](./get_trailingcharacter/)() const | Renvoie ou définit le caractère inséré après le numéro pour le niveau de liste. |
| static [GetEffectiveValue](./geteffectivevalue/)(int32_t, Aspose::Words::NumberStyle, const System::String\&) | Renvoie la représentation sous forme de chaîne de l'objet [ListLevel](./) pour l'index spécifié de l'élément de liste. Les paramètres spécifient le [NumberStyle](../../aspose.words/numberstyle/) et une chaîne de format optionnelle utilisée lorsque [Custom](../../aspose.words/numberstyle/) est spécifié. |
| [GetHashCode](./gethashcode/)() const override | Calcule le code de hachage pour cet objet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveTabStop](./removetabstop/)() | Supprime le point de tabulation du niveau de liste. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Lists::ListLevelAlignment) | Définisseur pour [Aspose::Words::Lists::ListLevel::get_Alignment](./get_alignment/). |
| [set_CustomNumberStyleFormat](./set_customnumberstyleformat/)(const System::String\&) | Définisseur pour [Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat](./get_customnumberstyleformat/). |
| [set_IsLegal](./set_islegal/)(bool) | Définisseur pour [Aspose::Words::Lists::ListLevel::get_IsLegal](./get_islegal/). |
| [set_LinkedStyle](./set_linkedstyle/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Définisseur pour [Aspose::Words::Lists::ListLevel::get_LinkedStyle](./get_linkedstyle/). |
| [set_NumberFormat](./set_numberformat/)(const System::String\&) | Définisseur pour [Aspose::Words::Lists::ListLevel::get_NumberFormat](./get_numberformat/). |
| [set_NumberPosition](./set_numberposition/)(double) | Définisseur pour [Aspose::Words::Lists::ListLevel::get_NumberPosition](./get_numberposition/). |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) | Définisseur pour [Aspose::Words::Lists::ListLevel::get_NumberStyle](./get_numberstyle/). |
| [set_RestartAfterLevel](./set_restartafterlevel/)(int32_t) | Définisseur pour [Aspose::Words::Lists::ListLevel::get_RestartAfterLevel](./get_restartafterlevel/). |
| [set_StartAt](./set_startat/)(int32_t) | Définisseur de [Aspose::Words::Lists::ListLevel::get_StartAt](./get_startat/). |
| [set_TabPosition](./set_tabposition/)(double) | Définisseur de [Aspose::Words::Lists::ListLevel::get_TabPosition](./get_tabposition/). |
| [set_TextPosition](./set_textposition/)(double) | Définisseur de [Aspose::Words::Lists::ListLevel::get_TextPosition](./get_textposition/). |
| [set_TrailingCharacter](./set_trailingcharacter/)(Aspose::Words::Lists::ListTrailingCharacter) | Définisseur de [Aspose::Words::Lists::ListLevel::get_TrailingCharacter](./get_trailingcharacter/). |
| static [Type](./type/)() |  |
## Remarques


Vous ne créez pas d'objets de cette classe. Les objets de niveau [List](../list/) sont créés automatiquement lorsqu'une liste est créée. Vous accédez aux objets [ListLevel](./) via la collection [ListLevelCollection](../listlevelcollection/).

Utilisez les propriétés de [ListLevel](./) pour spécifier le format de liste pour chaque niveau de liste.

## Exemples



Montre comment appliquer une mise en forme de liste personnalisée aux paragraphes lors de l’utilisation de [DocumentBuilder](../../aspose.words/documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Créez une liste à partir d’un modèle Microsoft Word et personnalisez les deux premiers niveaux de cette liste.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Cette valeur NumberFormat créera des symboles de puces en forme d’étoile.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Créez des paragraphes et appliquez les deux niveaux de notre mise en forme de liste personnalisée à ceux‑ci.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
