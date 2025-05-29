---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété CreateOutlinesForHeadingsInTables améliore l'organisation des tableaux en activant les contours pour les styles de titre, améliorant ainsi la clarté du document.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Spécifie s'il faut ou non créer des plans pour les titres (paragraphes formatés avec les styles de titre) à l'intérieur des tableaux.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## Remarques

La valeur par défaut est`FAUX`.

## Exemples

Montre comment créer des entrées de plan de document PDF pour les titres à l'intérieur des tableaux.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un tableau de trois lignes. La première ligne,
// dont le texte sera formaté dans un style de type titre, servira d'en-tête de colonne.
builder.StartTable();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("Customers");
builder.EndRow();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Write("John Doe");
builder.EndRow();
builder.InsertCell();
builder.Write("Jane Doe");
builder.EndTable();

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Le document PDF de sortie contiendra un plan, qui est une table des matières répertoriant les titres dans le corps du document.
// Cliquer sur une entrée dans ce plan nous amènera à l'emplacement de son titre respectif.
// Définissez la propriété « HeadingsOutlineLevels » sur « 1 » pour obtenir le contour
// pour enregistrer uniquement les titres dont les niveaux de titre ne sont pas supérieurs à 1.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Définissez la propriété « CreateOutlinesForHeadingsInTables » sur « false » pour exclure tous les titres des tableaux,
// tel que celui que nous avons créé ci-dessus à partir du contour.
// Définissez la propriété « CreateOutlinesForHeadingsInTables » sur « true » pour inclure tous les titres dans les tableaux
// dans le plan, à condition qu'ils aient un niveau de titre qui ne soit pas supérieur à la valeur de la propriété « HeadingsOutlineLevels ».
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Voir également

* class [OutlineOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
