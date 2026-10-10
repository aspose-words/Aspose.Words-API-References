---
title: "Aspose::Words::Fields::FieldBuilder::FieldBuilder constructeur"
linktitle: "FieldBuilder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldBuilder::FieldBuilder constructeur. Initialise une instance de la classe FieldBuilder en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder::FieldBuilder constructor


Initialise une instance de la classe [FieldBuilder](../).

```cpp
Aspose::Words::Fields::FieldBuilder::FieldBuilder(Aspose::Words::Fields::FieldType fieldType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Le type du champ à créer. |

## Exemples



Montre comment créer et insérer un champ à l'aide d'un constructeur de champ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Une façon pratique d'ajouter du texte à un document est d'utiliser un constructeur de document.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// Les champs ont leur constructeur, que nous pouvons utiliser pour construire le code d'un champ morceau par morceau.
// Dans ce cas, nous allons construire un champ BARCODE représentant un code postal US,
// et puis l'insérer devant un Run.
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## Voir aussi

* Enum [FieldType](../../fieldtype/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
