---
title: PdfSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words pour .NET
description: Découvrez la méthode PdfSaveOptions Clone pour créer sans effort un clone profond de vos objets, améliorant ainsi vos capacités de gestion PDF.
type: docs
weight: 370
url: /fr/net/aspose.words.saving/pdfsaveoptions/clone/
---
## PdfSaveOptions.Clone method

Crée un clone profond de cet objet.

```csharp
public PdfSaveOptions Clone()
```

## Exemples

Montre comment mettre à jour tous les champs d'un document immédiatement avant de l'enregistrer au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer du texte avec les champs PAGE et NUMPAGES. Ces champs n'affichent pas la valeur correcte en temps réel.
// Nous devrons les mettre à jour manuellement à l'aide de méthodes de mise à jour telles que « Field.Update() » et « Document.UpdateFields() »
// chaque fois que nous avons besoin qu'ils affichent des valeurs précises.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété « UpdateFields » sur « false » pour ne pas mettre à jour tous les champs d'un document juste avant une opération d'enregistrement.
// C'est l'option préférable si nous savons que tous nos champs seront à jour avant l'enregistrement.
// Définissez la propriété « UpdateFields » sur « true » pour parcourir tout le document
// champs et mettez-les à jour avant de sauvegarder le fichier PDF. Cela garantira l'affichage de tous les champs.
// les valeurs les plus précises du PDF.
options.UpdateFields = updateFields;

// Nous pouvons cloner des objets PdfSaveOptions.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
