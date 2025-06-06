---
title: FixedPageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words pour .NET
description: Contrôlez le rendu de vos documents avec FixedPageSaveOptions PageSet. Sélectionnez facilement des pages spécifiques ou sélectionnez-les toutes pour un rendu fluide. Optimisez votre flux de travail !
type: docs
weight: 70
url: /fr/net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

Obtient ou définit les pages à restituer. La valeur par défaut est toutes les pages du document.

```csharp
public PageSet PageSet { get; set; }
```

## Exemples

Montre comment extraire des pages en fonction d'index de page exacts.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez cinq pages au document.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Créez un objet « XpsSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Utilisez la propriété « PageSet » pour sélectionner un ensemble de pages du document à enregistrer dans la sortie XPS.
// Dans ce cas, nous choisirons, via un index de base zéro, seulement trois pages : page 1, page 2 et page 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

Montre comment convertir uniquement certaines pages d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
    // pour modifier la manière dont cette méthode convertit le document en .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Définissez « PageIndex » sur « 1 » pour restituer une partie du document à partir de la deuxième page.
    options.PageSet = new PageSet(1);

    // Ce document contiendra une page à partir de la page deux, qui ne contiendra que la deuxième page.
    doc.Save(stream, options);
}
```

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

* class [PageSet](../../pageset/)
* class [FixedPageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
