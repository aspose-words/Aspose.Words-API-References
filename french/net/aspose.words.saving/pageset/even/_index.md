---
title: PageSet.Even
linktitle: Even
articleTitle: Even
second_title: Aspose.Words pour .NET
description: Récupérez un ensemble de pages paires de votre document dans leur ordre d'origine avec PageSet Even. Optimisez votre flux de travail et optimisez la gestion de vos documents !
type: docs
weight: 30
url: /fr/net/aspose.words.saving/pageset/even/
---
## PageSet.Even property

Obtient un ensemble avec toutes les pages paires du document dans leur ordre d'origine.

```csharp
public static PageSet Even { get; }
```

## Remarques

Les pages paires ont des indices impairs puisque les indices de page sont basés sur zéro.

## Exemples

Montre comment exporter des pages impaires du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 5; i++)
{
    builder.Writeln($"Page {i + 1} ({(i % 2 == 0 ? "odd" : "even")})");
    if (i < 4)
        builder.InsertBreak(BreakType.PageBreak);
}

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Vous trouverez ci-dessous trois propriétés PageSet que nous pouvons utiliser pour filtrer un ensemble de pages à partir de
// notre document à enregistrer dans un document PDF de sortie en fonction de la parité de leurs numéros de page.
// 1 - Enregistrer uniquement les pages paires :
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 - Enregistrer uniquement les pages impaires :
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 - Enregistrer chaque page :
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### Voir également

* class [PageSet](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
