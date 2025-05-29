---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété PreserveFormFields de PdfSaveOptions conserve les champs de formulaire Microsoft Word dans les PDF ou les convertit en texte. Améliorez la qualité de vos documents !
type: docs
weight: 280
url: /fr/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Spécifie s'il faut conserver les champs de formulaire Microsoft Word en tant que champs de formulaire dans un PDF ou les convertir en texte. La valeur par défaut est`FAUX` .

```csharp
public bool PreserveFormFields { get; set; }
```

## Remarques

Les champs de formulaire Microsoft Word incluent des contrôles de saisie de texte, de liste déroulante et de case à cocher.

Lorsqu'il est réglé sur`FAUX` , ces champs seront exportés sous forme de texte au format PDF. Lorsque ce paramètre est défini sur`vrai`, ces champs seront exportés sous forme de champs de formulaire PDF.

Lors de l'exportation de champs de formulaire au format PDF en tant que champs de formulaire, une perte de formatage peut se produire car les champs PDF form ne prennent pas en charge toutes les fonctionnalités des champs de formulaire Microsoft Word.

De plus, la taille de sortie dépend de la taille du contenu, car les formulaires modifiables dans Microsoft Word sont des objets en ligne.

Les formulaires modifiables sont interdits par la conformité PDF/A.`FAUX` la valeur sera utilisée automatiquement lors de l'enregistrement au format PDF/A.

Les champs de formulaire ne sont pas pris en charge lors de l'enregistrement au format PDF/UA.`FAUX` la valeur sera utilisée automatiquement.

## Exemples

Montre comment enregistrer un document au format PDF à l'aide de la méthode Save et de la classe PdfSaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Insérer une zone de liste déroulante qui permettra à un utilisateur de choisir une option parmi une collection de chaînes.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Définissez la propriété « PreserveFormFields » sur « true » pour enregistrer les champs de formulaire en tant qu'objets interactifs dans le PDF de sortie.
// Définissez la propriété « PreserveFormFields » sur « false » pour geler tous les champs de formulaire du document à
// leurs valeurs actuelles et les afficher sous forme de texte brut dans le PDF de sortie.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
