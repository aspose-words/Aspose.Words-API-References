---
title: TextFormFieldType Enum
linktitle: TextFormFieldType
articleTitle: TextFormFieldType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Fields.TextFormFieldType, définissant différents types de champs de formulaire texte pour une automatisation et une personnalisation améliorées des documents.
type: docs
weight: 3180
url: /fr/net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

Spécifie le type d'un champ de formulaire texte.

```csharp
public enum TextFormFieldType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Regular | `0` | Le champ de formulaire de texte peut contenir n'importe quel texte. |
| Number | `1` | Le champ de formulaire de texte ne peut contenir que des chiffres. |
| Date | `2` | Le champ de formulaire de texte ne peut contenir qu'une valeur de date valide. |
| CurrentDate | `3` | La valeur du champ de formulaire de texte est la date actuelle à laquelle le champ est mis à jour. |
| CurrentTime | `4` | La valeur du champ de formulaire de texte est l'heure actuelle à laquelle le champ est mis à jour. |
| Calculated | `5` | La valeur du champ de formulaire de texte est calculée à partir de l'expression spécifiée dans le[`TextInputDefault`](../formfield/textinputdefault/) propriété. |

## Exemples

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

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
