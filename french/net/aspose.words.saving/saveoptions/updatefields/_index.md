---
title: SaveOptions.UpdateFields
second_title: Référence de l'API Aspose.Words pour .NET
description: SaveOptions propriété. Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant denregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété estvrai .
type: docs
weight: 160
url: /fr/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est`vrai` .

```csharp
public bool UpdateFields { get; set; }
```

### Remarques

Permet de spécifier s'il faut imiter ou non le comportement de MS Word.

### Exemples

Montre comment mettre à jour tous les champs d'un document immédiatement avant de l'enregistrer au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère du texte avec les champs PAGE et NUMPAGES. Ces champs n'affichent pas la bonne valeur en temps réel.
// Nous devrons les mettre à jour manuellement en utilisant des méthodes de mise à jour telles que "Field.Update()" et "Document.UpdateFields()"
// chaque fois que nous en avons besoin pour afficher des valeurs précises.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "UpdateFields" sur "false" pour ne pas mettre à jour tous les champs d'un document juste avant une opération de sauvegarde.
// C'est l'option préférable si l'on sait que tous nos champs seront à jour avant de sauvegarder.
// Définissez la propriété "UpdateFields" sur "true" pour parcourir tout le document
// champs et mettez-les à jour avant de l'enregistrer au format PDF. Cela garantira que tous les champs s'afficheront
// les valeurs les plus précises du PDF.
options.UpdateFields = updateFields;

// Nous pouvons cloner des objets PdfSaveOptions.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../saveoptions/)
* Assemblée [Aspose.Words](../../../)


