---
title: "Méthode Aspose::Words::DocumentBuilder::InsertTextInput"
linktitle: "InsertTextInput"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::InsertTextInput. Insère un champ de formulaire texte à la position actuelle en C++."
type: docs
weight: 49000
url: /fr/cpp/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder::InsertTextInput method


Insère un champ de formulaire texte à la position actuelle.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertTextInput(const System::String &name, Aspose::Words::Fields::TextFormFieldType type, const System::String &format, const System::String &fieldValue, int32_t maxLength)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom du champ de formulaire. Peut être une chaîne vide. |
| type | Aspose::Words::Fields::TextFormFieldType | Spécifie le type du champ de formulaire texte. |
| format | const System::String\& | Chaîne de format utilisée pour formater la valeur du champ de formulaire. |
| fieldValue | const System::String\& | Texte qui sera affiché dans le champ. |
| maxLength | int32_t | Longueur maximale que l'utilisateur peut saisir dans le champ de formulaire. Réglez à zéro pour une longueur illimitée. |

### ReturnValue

Le nœud du champ de formulaire qui vient d'être inséré.
## Remarques


Si vous spécifiez un nom pour le champ de formulaire, un signet est alors créé automatiquement avec le même nom.

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


Montre comment insérer un champ de formulaire texte dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un formulaire qui invite l'utilisateur à saisir du texte.
builder->InsertTextInput(u"TextInput", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your text here", 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTextInput.docx");
```


Montre comment insérer un champ de formulaire texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please enter text here: ");

// Insérez un champ de saisie texte, qui permettra à l'utilisateur de cliquer dessus et de saisir du texte.
// Attribuez un texte d'espace réservé que l'utilisateur peut écraser et transmettre
// une longueur maximale de texte de 0 pour ne pas appliquer de limite au contenu du champ de formulaire.
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Le champ de formulaire apparaîtra sous la forme d'une balise html "input", avec un type "text".
doc->Save(get_ArtifactsDir() + u"FormFields.TextInput.html");
```

## Voir aussi

* Class [FormField](../../../aspose.words.fields/formfield/)
* Enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
