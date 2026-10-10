---
title: "Aspose::Words::DocumentBuilder::InsertComboBox method"
linktitle: "InsertComboBox"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertComboBox method. Insère un champ de formulaire de type liste déroulante à la position actuelle en C++."
type: docs
weight: 32000
url: /fr/cpp/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder::InsertComboBox method


Insère un champ de formulaire combo box à la position actuelle.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertComboBox(const System::String &name, const System::ArrayPtr<System::String> &items, int32_t selectedIndex)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom du champ de formulaire. Peut être une chaîne vide. La valeur de plus de 20 caractères sera tronquée. |
| items | const System::ArrayPtr\<System::String\>\& | Les éléments de la ComboBox. Le maximum est de 25 éléments. |
| selectedIndex | int32_t | L'index de l'élément sélectionné dans la ComboBox. |

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


Montre comment insérer un champ de formulaire de type liste déroulante dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez un formulaire qui invite l'utilisateur à choisir l'un des éléments du menu.
builder->Write(u"Pick a fruit: ");
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"});
builder->InsertComboBox(u"DropDown", items, 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertComboBox.docx");
```

## Voir aussi

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
