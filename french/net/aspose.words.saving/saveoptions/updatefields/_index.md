---
title: SaveOptions.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété SaveOptions UpdateFields optimise l'enregistrement des documents en mettant à jour des types de champs spécifiques avant la conversion vers des formats fixes. Valeur par défaut  true.
type: docs
weight: 170
url: /fr/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est`vrai` .

```csharp
public bool UpdateFields { get; set; }
```

## Remarques

Permet de spécifier s'il faut imiter ou non le comportement de MS Word.

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

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
