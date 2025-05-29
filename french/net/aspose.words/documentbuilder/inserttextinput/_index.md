---
title: DocumentBuilder.InsertTextInput
linktitle: InsertTextInput
articleTitle: InsertTextInput
second_title: Aspose.Words pour .NET
description: Ajoutez facilement des champs de texte à vos formulaires grâce à la méthode InsertTextInput de DocumentBuilder. Améliorez l'interactivité et l'expérience utilisateur de vos documents dès aujourd'hui !
type: docs
weight: 510
url: /fr/net/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder.InsertTextInput method

Insère un champ de formulaire de texte à la position actuelle.

```csharp
public FormField InsertTextInput(string name, TextFormFieldType type, string format, 
    string fieldValue, int maxLength)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Nom du champ de formulaire. Peut être une chaîne vide. |
| type | TextFormFieldType | Spécifie le type du champ de formulaire de texte. |
| format | String | Chaîne de format utilisée pour formater la valeur du champ de formulaire. |
| fieldValue | String | Texte qui sera affiché dans le champ. |
| maxLength | Int32 | Longueur maximale que l'utilisateur peut saisir dans le champ du formulaire. Définissez-la sur zéro pour une longueur illimitée. |

### Return_Value

Le nœud de champ de formulaire qui vient d’être inséré.

## Remarques

Si vous spécifiez un nom pour le champ de formulaire, un signet est automatiquement créé avec le même nom.

## Exemples

Montre comment insérer un champ de formulaire de saisie de texte dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un formulaire qui invite l'utilisateur à saisir du texte.
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

Montre comment insérer un champ de formulaire de saisie de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// Insérer un champ de saisie de texte, qui permettra à l'utilisateur de cliquer dessus et de saisir du texte.
// Attribuer un texte d'espace réservé que l'utilisateur peut écraser et transmettre
// une longueur de texte maximale de 0 pour n'appliquer aucune limite au contenu du champ de formulaire.
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Le champ de formulaire apparaîtra sous la forme d'une balise HTML « input », avec un type « texte ».
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
```

Montre comment créer des champs de formulaire.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Les champs de formulaire sont des objets du document avec lesquels l'utilisateur peut interagir en étant invité à saisir des valeurs.
// Nous pouvons les créer à l'aide d'un générateur de documents, et vous trouverez ci-dessous deux manières de le faire.
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

* class [FormField](../../../aspose.words.fields/formfield/)
* enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
