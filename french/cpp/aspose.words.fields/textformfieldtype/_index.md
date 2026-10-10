---
title: "Énumération Aspose::Words::Fields::TextFormFieldType"
linktitle: "TextFormFieldType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::Fields::TextFormFieldType. Spécifie le type d'un champ de formulaire texte en C++."
type: docs
weight: 134000
url: /fr/cpp/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enum


Spécifie le type d’un champ de formulaire texte.

```cpp
enum class TextFormFieldType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Regular | 0 | Le champ de formulaire texte peut contenir n'importe quel texte. |
| Nombre | 1 | Le champ de formulaire texte ne peut contenir que des nombres. |
| Date | 2 | Le champ de formulaire texte ne peut contenir qu'une valeur de date valide. |
| CurrentDate | 3 | La valeur du champ de formulaire texte est la date actuelle lorsque le champ est mis à jour. |
| CurrentTime | 4 | La valeur du champ de formulaire texte est l'heure actuelle lorsque le champ est mis à jour. |
| Calculated | 5 | La valeur du champ de formulaire texte est calculée à partir de l'expression spécifiée dans la propriété [TextInputDefault](../formfield/get_textinputdefault/). |


## Exemples



Montre comment créer des champs de formulaire.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Les champs de formulaire sont des objets du document avec lesquels l'utilisateur peut interagir en étant invité à saisir des valeurs.
// Nous pouvons les créer à l'aide d'un constructeur de document, et voici deux façons de le faire.
// 1 -  Entrée de texte de base :
builder->InsertTextInput(u"My text input", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your name here", 30);

// 2 -  Boîte combinée avec texte d'invite, et une plage de valeurs possibles :
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"-- Select your favorite footwear --", u"Sneakers", u"Oxfords", u"Flip-flops", u"Other"});

builder->InsertParagraph();
builder->InsertComboBox(u"My combo box", items, 0);

builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateForm.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
