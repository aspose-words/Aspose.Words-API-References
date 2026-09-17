---
title: "Méthode Aspose::Words::Paragraph::InsertField"
linktitle: "InsertField"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Paragraph::InsertField. Insère un champ dans ce paragraphe en C++."
type: docs
weight: 29000
url: /fr/cpp/aspose.words/paragraph/insertfield/
---
## Paragraph::InsertField(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Insère un champ dans ce paragraphe.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(Aspose::Words::Fields::FieldType fieldType, bool updateField, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Le type du champ à insérer. |
| updateField | bool | Spécifie si le champ doit être mis à jour immédiatement. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Nœud de référence à l'intérieur de ce paragraphe (si *refNode* est **null**, alors il s'ajoute à la fin du paragraphe). |
| isAfter | bool | Indique s'il faut insérer le champ après ou avant le nœud de référence. |

### ReturnValue

Un objet [Field](../../../aspose.words.fields/field/) qui représente le champ inséré.

## Exemples



Présente diverses manières d'ajouter des champs à un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Voici trois façons d'insérer un champ dans un paragraphe.
// 1 -  Insérer un champ AUTHOR dans un paragraphe après l'un des nœuds enfants du paragraphe :
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Insérer un champ QUOTE après l'un des nœuds enfants du paragraphe :
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Insérer un champ QUOTE avant l'un des nœuds enfants du paragraphe ,
// et le faire afficher une valeur de substitution :
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Ce champ affichera sa valeur de substitution jusqu'à ce que nous le mettions à jour.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Voir aussi

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Insère un champ dans ce paragraphe.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | Le code de champ à insérer (sans accolades). |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Nœud de référence à l'intérieur de ce paragraphe (si *refNode* est **null**, alors il s'ajoute à la fin du paragraphe). |
| isAfter | bool | Indique s'il faut insérer le champ après ou avant le nœud de référence. |

### ReturnValue

Un objet [Field](../../../aspose.words.fields/field/) qui représente le champ inséré.

## Exemples



Présente diverses manières d'ajouter des champs à un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Voici trois façons d'insérer un champ dans un paragraphe.
// 1 -  Insérer un champ AUTHOR dans un paragraphe après l'un des nœuds enfants du paragraphe :
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Insérer un champ QUOTE après l'un des nœuds enfants du paragraphe :
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Insérer un champ QUOTE avant l'un des nœuds enfants du paragraphe ,
// et le faire afficher une valeur de substitution :
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Ce champ affichera sa valeur de substitution jusqu'à ce que nous le mettions à jour.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Voir aussi

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::InsertField(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Insère un champ dans ce paragraphe.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::InsertField(const System::String &fieldCode, const System::String &fieldValue, const System::SharedPtr<Aspose::Words::Node> &refNode, bool isAfter)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | Le code de champ à insérer (sans accolades). |
| fieldValue | const System::String\& | La valeur du champ à insérer. Passez **null** pour les champs qui n'ont pas de valeur. |
| refNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Nœud de référence à l'intérieur de ce paragraphe (si *refNode* est **null**, alors il s'ajoute à la fin du paragraphe). |
| isAfter | bool | Indique s'il faut insérer le champ après ou avant le nœud de référence. |

### ReturnValue

Un objet [Field](../../../aspose.words.fields/field/) qui représente le champ inséré.

## Exemples



Présente diverses manières d'ajouter des champs à un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Voici trois façons d'insérer un champ dans un paragraphe.
// 1 -  Insérer un champ AUTHOR dans un paragraphe après l'un des nœuds enfants du paragraphe :
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"This run was written by ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_BuiltInDocumentProperties()->idx_get(u"Author")->set_Value(System::ExplicitCast<System::Object>(u"John Doe"));
para->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true, run, true);

// 2 -  Insérer un champ QUOTE après l'un des nœuds enfants du paragraphe :
run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u".");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

System::SharedPtr<Aspose::Words::Fields::Field> field = para->InsertField(u" QUOTE \" Real value\" ", run, true);

// 3 -  Insérer un champ QUOTE avant l'un des nœuds enfants du paragraphe ,
// et le faire afficher une valeur de substitution :
para->InsertField(u" QUOTE \" Real value.\"", u" Placeholder value.", field->get_Start(), false);

ASSERT_EQ(u" Placeholder value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Ce champ affichera sa valeur de substitution jusqu'à ce que nous le mettions à jour.
doc->UpdateFields();

ASSERT_EQ(u" Real value.", doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.InsertField.docx");
```

## Voir aussi

* Class [Field](../../../aspose.words.fields/field/)
* Class [Node](../../node/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
