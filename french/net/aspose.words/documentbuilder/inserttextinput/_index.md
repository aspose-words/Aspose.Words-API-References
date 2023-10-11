---
title: DocumentBuilder.InsertTextInput
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Insère un champ de formulaire texte à la position actuelle.
type: docs
weight: 480
url: /fr/net/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder.InsertTextInput method

Insère un champ de formulaire texte à la position actuelle.

```csharp
public FormField InsertTextInput(string name, TextFormFieldType type, string format, 
    string fieldValue, int maxLength)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Le nom du champ du formulaire. Peut être une chaîne vide. |
| type | TextFormFieldType | Spécifie le type du champ du formulaire de texte. |
| format | String | Chaîne de format utilisée pour formater la valeur du champ du formulaire. |
| fieldValue | String | Texte qui sera affiché dans le champ. |
| maxLength | Int32 | Longueur maximale que l'utilisateur peut saisir dans le champ du formulaire. Réglé à zéro pour une longueur illimitée. |

### Return_Value

Le nœud du champ de formulaire qui vient d’être inséré.

### Remarques

Si vous spécifiez un nom pour le champ du formulaire, un signet est automatiquement créé avec le même nom.

### Exemples

Montre comment insérer un champ de formulaire de saisie de texte dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un formulaire qui invite l'utilisateur à saisir du texte.
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

Montre comment insérer un champ de formulaire de saisie de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// Insère un champ de saisie de texte, qui permettra à l'utilisateur de cliquer dessus et de saisir du texte.
// Attribue un texte d'espace réservé que l'utilisateur peut écraser et transmettre
// une longueur de texte maximale de 0 pour n'appliquer aucune limite au contenu du champ du formulaire.
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Le champ du formulaire apparaîtra sous la forme d'une balise html "input", de type "texte".
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
```

Montre comment créer des champs de formulaire.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Les champs de formulaire sont des objets du document avec lesquels l'utilisateur peut interagir en étant invité à saisir des valeurs.
// Nous pouvons les créer à l'aide d'un générateur de documents, et vous trouverez ci-dessous deux façons de le faire.
// 1 - Saisie de texte de base :
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - Zone de liste déroulante avec un texte d'invite et une plage de valeurs possibles :
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
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


