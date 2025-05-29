---
title: PdfSaveOptions.UseSdtTagAsFormFieldName
linktitle: UseSdtTagAsFormFieldName
articleTitle: UseSdtTagAsFormFieldName
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété PdfSaveOptions UseSdtTagAsFormFieldName améliore les formulaires PDF en utilisant des balises de contrôle SDT pour une meilleure organisation et clarté.
type: docs
weight: 340
url: /fr/net/aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/
---
## PdfSaveOptions.UseSdtTagAsFormFieldName property

Spécifie s'il faut utiliser la balise de contrôle SDT ou la propriété Id comme nom de champ de formulaire dans le PDF.

```csharp
public bool UseSdtTagAsFormFieldName { get; set; }
```

## Remarques

La valeur par défaut est`FAUX`.

Lorsqu'il est réglé sur`FAUX`La propriété d'ID de contrôle SDT est utilisée comme nom de champ de formulaire dans PDF.

Lorsqu'il est réglé sur`vrai`La propriété de balise de contrôle SDT est utilisée comme nom de champ de formulaire dans PDF.

Si défini sur`vrai` et la balise est vide, la propriété Id sera utilisée comme nom de champ de formulaire.

Si défini sur`vrai` et les valeurs de balise ne sont pas uniques, les valeurs de balise en double seront modifiées en noms de champs de formulaire PDF uniques.

## Exemples

Montre comment utiliser la propriété Tag ou Id du contrôle SDT comme nom de champ de formulaire dans un PDF.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
// Lorsqu'il est défini sur « false », la propriété d'ID de contrôle SDT est utilisée comme nom de champ de formulaire dans PDF.
// Lorsqu'elle est définie sur « true », la propriété Tag de contrôle SDT est utilisée comme nom de champ de formulaire dans PDF.
saveOptions.UseSdtTagAsFormFieldName = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.SdtTagAsFormFieldName.pdf", saveOptions);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
