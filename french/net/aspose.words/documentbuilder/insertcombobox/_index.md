---
title: InsertComboBox
second_title: Référence de l'API Aspose.Words pour .NET
description: Insère un champ de formulaire combobox à la position actuelle.
type: docs
weight: 280
url: /fr/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

Insère un champ de formulaire combobox à la position actuelle.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Nom du champ de formulaire. Peut être une chaîne vide. La valeur supérieure à 20 caractères sera tronquée. |
| items | String[] | Les éléments du ComboBox. Le maximum est de 25 éléments. |
| selectedIndex | Int32 | L'index de l'élément sélectionné dans le ComboBox. |

### Return_Value

Le nœud de champ de formulaire qui vient d'être inséré.

### Remarques

Si vous spécifiez un nom pour le champ de formulaire, un signet est automatiquement créé avec le même nom.

### Exemples

Montre comment insérer un champ de formulaire de zone de liste déroulante dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un formulaire qui invite l'utilisateur à choisir l'un des éléments du menu.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

Montre comment créer des champs de formulaire.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Les champs de formulaire sont des objets du document avec lesquels l'utilisateur peut interagir en étant invité à saisir des valeurs.
// Nous pouvons les créer à l'aide d'un générateur de documents, et ci-dessous sont deux façons de le faire.
// 1 - Saisie de texte de base :
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Zone de liste déroulante avec texte d'invite et une plage de valeurs possibles :
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### Voir également

* class [FormField](../../../aspose.words.fields/formfield)
* class [DocumentBuilder](../../documentbuilder)
* espace de noms [Aspose.Words](../../documentbuilder)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->