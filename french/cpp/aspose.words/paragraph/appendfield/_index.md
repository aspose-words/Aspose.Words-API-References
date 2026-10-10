---
title: "Méthode Aspose::Words::Paragraph::AppendField"
linktitle: "AppendField"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Paragraph::AppendField. Ajoute un champ à ce paragraphe en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/paragraph/appendfield/
---
## Paragraph::AppendField(Aspose::Words::Fields::FieldType, bool) method


Ajoute un champ à ce paragraphe.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(Aspose::Words::Fields::FieldType fieldType, bool updateField)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Le type du champ à ajouter. |
| updateField | bool | Spécifie si le champ doit être mis à jour immédiatement. |

### ReturnValue

Un objet [Field](../../../aspose.words.fields/field/) qui représente le champ ajouté.

## Exemples



Présente différentes manières d'ajouter des champs à un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Voici trois façons d'ajouter un champ à la fin d'un paragraphe.
// 1 -  Ajoutez un champ DATE en utilisant un type de champ, puis mettez-le à jour :
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Ajoutez un champ TIME en utilisant un code de champ :
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Ajoutez un champ QUOTE en utilisant un code de champ, et faites-le afficher une valeur de substitution :
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Ce champ affichera sa valeur de substitution jusqu'à ce que nous le mettions à jour.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Voir aussi

* Class [Field](../../../aspose.words.fields/field/)
* Enum [FieldType](../../../aspose.words.fields/fieldtype/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&) method


Ajoute un champ à ce paragraphe.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | Le code du champ à ajouter (sans accolades). |

### ReturnValue

Un objet [Field](../../../aspose.words.fields/field/) qui représente le champ ajouté.

## Exemples



Présente différentes manières d'ajouter des champs à un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Voici trois façons d'ajouter un champ à la fin d'un paragraphe.
// 1 -  Ajoutez un champ DATE en utilisant un type de champ, puis mettez-le à jour :
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Ajoutez un champ TIME en utilisant un code de champ :
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Ajoutez un champ QUOTE en utilisant un code de champ, et faites-le afficher une valeur de substitution :
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Ce champ affichera sa valeur de substitution jusqu'à ce que nous le mettions à jour.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Voir aussi

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::AppendField(const System::String\&, const System::String\&) method


Ajoute un champ à ce paragraphe.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::Paragraph::AppendField(const System::String &fieldCode, const System::String &fieldValue)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldCode | const System::String\& | Le code du champ à ajouter (sans accolades). |
| fieldValue | const System::String\& | La valeur du champ à ajouter. Passez **null** pour les champs qui n'ont pas de valeur. |

### ReturnValue

Un objet [Field](../../../aspose.words.fields/field/) qui représente le champ ajouté.

## Exemples



Présente différentes manières d'ajouter des champs à un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Voici trois façons d'ajouter un champ à la fin d'un paragraphe.
// 1 -  Ajoutez un champ DATE en utilisant un type de champ, puis mettez-le à jour :
paragraph->AppendField(Aspose::Words::Fields::FieldType::FieldDate, true);

// 2 -  Ajoutez un champ TIME en utilisant un code de champ :
paragraph->AppendField(u" TIME  \\@ \"HH:mm:ss\" ");

// 3 -  Ajoutez un champ QUOTE en utilisant un code de champ, et faites-le afficher une valeur de substitution :
paragraph->AppendField(u" QUOTE \"Real value\"", u"Placeholder value");

ASSERT_EQ(u"Placeholder value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

// Ce champ affichera sa valeur de substitution jusqu'à ce que nous le mettions à jour.
doc->UpdateFields();

ASSERT_EQ(u"Real value", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());

doc->Save(get_ArtifactsDir() + u"Paragraph.AppendField.docx");
```

## Voir aussi

* Class [Field](../../../aspose.words.fields/field/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
