---
title: PdfSaveOptions.Clone
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions méthode. Crée un clone profond de cet objet.
type: docs
weight: 310
url: /fr/net/aspose.words.saving/pdfsaveoptions/clone/
---
## PdfSaveOptions.Clone method

Crée un clone profond de cet objet.

```csharp
public PdfSaveOptions Clone()
```

### Exemples

Montre comment mettre à jour tous les champs d'un document immédiatement avant de l'enregistrer au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer du texte avec les champs PAGE et NUMPAGES. Ces champs n'affichent pas la valeur correcte en temps réel.
// Nous devrons les mettre à jour manuellement en utilisant des méthodes de mise à jour telles que "Field.Update()" et "Document.UpdateFields()"
// chaque fois que nous en avons besoin pour afficher des valeurs précises.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "UpdateFields" sur "false" pour ne pas mettre à jour tous les champs d'un document juste avant une opération de sauvegarde.
// C'est l'option préférable si nous savons que tous nos champs seront à jour avant d'enregistrer.
// Définissez la propriété "UpdateFields" sur "true" pour parcourir tout le document
// champs et mettez-les à jour avant de l'enregistrer au format PDF. Cela garantira que tous les champs s'afficheront
// les valeurs les plus précises dans le PDF.
options.UpdateFields = updateFields;

// Nous pouvons cloner des objets PdfSaveOptions.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


