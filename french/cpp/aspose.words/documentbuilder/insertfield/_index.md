---
title: "Aspose::Words::DocumentBuilder::InsertField méthode"
linktitle: "InsertField"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertField méthode. Insère un champ Word dans un document et met éventuellement à jour le résultat du champ en C++."
type: docs
weight: 34000
url: /fr/cpp/aspose.words/documentbuilder/insertfield/
---
## DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType, bool) method


Insère un champ Word dans un document et met éventuellement à jour le résultat du champ.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Le type du champ à ajouter. |
| updateField | bool | Spécifie si le champ doit être mis à jour immédiatement. |

### ReturnValue

Un objet [Field](../../../aspose.words.fields/field/) qui représente le champ inséré.
## Remarques


Cette méthode insère un champ dans un document. Aspose.Words peut mettre à jour les champs de la plupart des types, mais pas tous. Pour plus de détails, voir la surcharge [InsertField()](../).

## Exemples



Montre comment insérer un champ dans un document en utilisant FieldType.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez deux champs en passant un indicateur qui détermine s'ils doivent être mis à jour pendant que le constructeur les insère.
// Dans certains cas, la mise à jour des champs peut être coûteuse en calcul, et il peut être judicieux de différer la mise à jour.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
builder->Write(u"This document was written by ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, updateInsertedFieldsImmediately);

builder->InsertParagraph();
builder->Write(u"\nThis is page ");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, updateInsertedFieldsImmediately);

ASSERT_EQ(u" AUTHOR ", doc->get_Range()->get_Fields()->idx_get(0)->GetFieldCode());
ASSERT_EQ(u" PAGE ", doc->get_Range()->get_Fields()->idx_get(1)->GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
else
{
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

    // Nous devrons mettre à jour ces champs en utilisant les méthodes de mise à jour manuellement.
    doc->get_Range()->get_Fields()->idx_get(0)->Update();

    ASSERT_EQ(u"John Doe", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

    doc->UpdateFields();

    ASSERT_EQ(u"1", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
}
```

## Voir aussi

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&) method


Insère un champ Word dans un document et met à jour le résultat du champ.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | Le code de champ à insérer (sans accolades). |

### ReturnValue

Un objet [Field](../../../aspose.words.fields/field/) qui représente le champ inséré.
## Remarques


Cette méthode insère un champ dans un document et met à jour le résultat du champ immédiatement. Aspose.Words peut mettre à jour les champs de la plupart des types, mais pas tous. Pour plus de détails, voir la surcharge [InsertField()](../).

## Exemples



Montre comment insérer des champs et déplacer le curseur du constructeur de document vers eux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// Déplacez le curseur vers le premier MERGEFIELD.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// Notez que le curseur est placé immédiatement après le premier MERGEFIELD, et avant le deuxième.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// Si nous souhaitons modifier le code de champ ou le contenu du champ à l'aide du constructeur,
// son curseur devrait être à l'intérieur d'un champ.
// Pour le placer à l'intérieur d'un champ, nous devrions appeler la méthode MoveTo du constructeur de document
// et passer le nœud de début ou de séparateur du champ comme argument.
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```


Montre comment insérer un champ dans un document à l'aide d'un code de champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Cette surcharge de la méthode InsertField met automatiquement à jour les champs insérés.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Voir aussi

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertField(const System::String\&, const System::String\&) method


Insère un champ Word dans un document sans mettre à jour le résultat du champ.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertField(const System::String &fieldCode, const System::String &fieldValue)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | Le code de champ à insérer (sans accolades). |
| fieldValue | const System::String\& | La valeur du champ à insérer. Passez **null** pour les champs qui n'ont pas de valeur. |

### ReturnValue

Un objet [Field](../../../aspose.words.fields/field/) qui représente le champ inséré.
## Remarques


[Fields](../../../aspose.words.fields/) in Microsoft Word documents consist of a field code and a field result. The field code is like a formula and the field result is like the value that the formula produces. The field code may also contain field switches that are like additional instructions to perform a specific action.

Vous pouvez basculer entre l'affichage des codes de champ et des résultats dans votre document dans Microsoft Word en utilisant le raccourci clavier Alt+F9. Les codes de champ apparaissent entre accolades ( { } ).

Pour créer un champ, vous devez spécifier un type de champ, un code de champ et une valeur de champ "placeholder". Si vous n'êtes pas sûr de la syntaxe d'un code de champ particulier, créez d'abord le champ dans Microsoft Word puis basculez pour voir son code de champ.

Aspose.Words peut calculer les résultats des champs pour la plupart des types de champs, mais cette méthode ne met pas à jour le résultat du champ automatiquement. Comme le résultat du champ n'est pas calculé automatiquement, vous devez fournir une valeur de chaîne (ou même une chaîne vide) qui sera insérée dans le résultat du champ. Cette valeur restera dans le résultat du champ comme espace réservé jusqu'à ce que le champ soit mis à jour. Pour mettre à jour le résultat du champ, vous pouvez appeler [Update](../../../aspose.words.fields/field/update/) sur l'objet champ qui vous est retourné ou [UpdateFields](../../document/updatefields/) pour mettre à jour les champs dans l'ensemble du document.

## Exemples



Montre comment configurer la numérotation des pages dans une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Déplacez le constructeur de document vers l'en-tête principal de la première section,
// qui sera affiché sur chaque page de cette section.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Insérez un champ PAGE, qui affichera le numéro de la page actuelle.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Configurez la section pour que le nombre de pages affiché par les champs PAGE commence à 5.
// De plus, configurez tous les champs PAGE pour afficher leurs numéros de page en chiffres romains majuscules.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Créez un autre en-tête principal pour la deuxième section, avec un autre champ PAGE.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Configurez la section pour que le nombre de pages affiché par les champs PAGE commence à 10.
// De plus, configurez tous les champs PAGE pour afficher leurs numéros de page en chiffres arabes.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Voir aussi

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
