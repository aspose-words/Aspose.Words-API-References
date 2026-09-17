---
title: "Aspose::Words::Fields::Field::Update méthode"
linktitle: "Mettre à jour"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::Field::Update méthode. Effectue la mise à jour du champ. Lève une exception si le champ est déjà en cours de mise à jour en C++."
type: docs
weight: 23000
url: /fr/cpp/aspose.words.fields/field/update/
---
## Field::Update() method


Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour.

```cpp
void Aspose::Words::Fields::Field::Update()
```


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


Montre comment formater les résultats de champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilisez un constructeur de document pour insérer un champ qui affiche un résultat sans aucun format appliqué.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// Nous pouvons appliquer un format au résultat d'un champ en utilisant les propriétés du champ.
// Voici trois types de formats que nous pouvons appliquer au résultat d'un champ.
// 1 -  Format numérique :
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 -  Format date/heure :
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 -  Format général :
field = builder->InsertField(u"= 25 + 33");
format = field->get_Format();
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::Upper);
field->Update();

int32_t index = 0;
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<Aspose::Words::Fields::GeneralFormat>> generalFormatEnumerator = format->get_GeneralFormats()->GetEnumerator();
    while (generalFormatEnumerator->MoveNext())
    {
        std::cout << System::String::Format(u"General format index {0}: {1}", index++, generalFormatEnumerator->get_Current()) << std::endl;
    }
}

ASSERT_EQ(u"= 25 + 33 \\* roman \\* Upper", field->GetFieldCode());
ASSERT_EQ(u"LVIII", field->get_Result());
ASSERT_EQ(2, format->get_GeneralFormats()->get_Count());
ASSERT_EQ(Aspose::Words::Fields::GeneralFormat::LowercaseRoman, format->get_GeneralFormats()->idx_get(0));

// Nous pouvons supprimer nos formats pour ramener le résultat du champ à sa forme originale.
format->get_GeneralFormats()->Remove(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
```

## Voir aussi

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::Update(bool) method


Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour.

```cpp
void Aspose::Words::Fields::Field::Update(bool ignoreMergeFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | bool | Si **true** alors le formatage direct du résultat du champ est abandonné, quel que soit le commutateur MERGEFORMAT, sinon une mise à jour normale est effectuée. |

## Exemples



Montre comment conserver ou ignorer les champs INCLUDEPICTURE lors du chargement d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto includePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx));

    // Nous pouvons définir un indicateur dans un objet LoadOptions pour décider s'il faut convertir tous les champs INCLUDEPICTURE
    // en formes image lors du chargement d'un document qui les contient.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_PreserveIncludePictureField(preserveIncludePictureField);

    doc = System::MakeObject<Aspose::Words::Document>(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        ASSERT_TRUE(doc->get_Range()->get_Fields()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
        {
            return f->get_Type() == Aspose::Words::Fields::FieldType::FieldIncludePicture;
        }))));

        doc->UpdateFields();
        doc->Save(get_ArtifactsDir() + u"Field.PreserveIncludePicture.docx");
    }
    else
    {
        ASSERT_FALSE(doc->get_Range()->get_Fields()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
        {
            return f->get_Type() == Aspose::Words::Fields::FieldType::FieldIncludePicture;
        }))));
    }
}
```

## Voir aussi

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
