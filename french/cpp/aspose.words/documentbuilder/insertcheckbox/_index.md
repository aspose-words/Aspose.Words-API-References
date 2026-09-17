---
title: "Méthode Aspose::Words::DocumentBuilder::InsertCheckBox"
linktitle: "InsertCheckBox"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::InsertCheckBox. Insère un champ de formulaire case à cocher à la position actuelle en C++."
type: docs
weight: 31000
url: /fr/cpp/aspose.words/documentbuilder/insertcheckbox/
---
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, int32_t) method


Insère un champ de formulaire case à cocher à la position actuelle.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool checkedValue, int32_t size)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom du champ de formulaire. Peut être une chaîne vide. La valeur de plus de 20 caractères sera tronquée. |
| checkedValue | bool | État coché du champ de formulaire case à cocher. |
| size | int32_t | Spécifie la taille de la case à cocher en points. Spécifiez 0 pour que MS Word calcule automatiquement la taille de la case à cocher. |

### ReturnValue

Le nœud du champ de formulaire qui vient d'être inséré.
## Remarques


Si vous spécifiez un nom pour le champ de formulaire, un signet est alors créé automatiquement avec le même nom.

## Exemples



Montre comment insérer des cases à cocher dans le document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez des cases à cocher de tailles variables et d'états cochés par défaut.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Les champs de formulaire ont une limite de longueur de nom de 20 caractères.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Nous pouvons interagir avec ces cases à cocher dans Microsoft Word en double-cliquant dessus.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Voir aussi

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, bool, int32_t) method


Insère un champ de formulaire case à cocher à la position actuelle.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool defaultValue, bool checkedValue, int32_t size)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom du champ de formulaire. Peut être une chaîne vide. La valeur de plus de 20 caractères sera tronquée. |
| defaultValue | bool | Valeur par défaut du champ de formulaire de case à cocher. |
| checkedValue | bool | État coché actuel du champ de formulaire de case à cocher. |
| size | int32_t | Spécifie la taille de la case à cocher en points. Spécifiez 0 pour que MS Word calcule automatiquement la taille de la case à cocher. |

### ReturnValue

Le nœud du champ de formulaire qui vient d'être inséré.
## Remarques


Si vous spécifiez un nom pour le champ de formulaire, un signet est alors créé automatiquement avec le même nom.

## Exemples



Montre comment insérer des cases à cocher dans le document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez des cases à cocher de tailles variables et d'états cochés par défaut.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Les champs de formulaire ont une limite de longueur de nom de 20 caractères.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Nous pouvons interagir avec ces cases à cocher dans Microsoft Word en double-cliquant dessus.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Voir aussi

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
