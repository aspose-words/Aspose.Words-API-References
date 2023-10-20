---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: Aspose.Words pour .NET
description: PdfSaveOptions UseCoreFonts propriété. Obtient ou définit une valeur déterminant sil faut ou non remplacer les polices TrueType Arial Times New Roman Courier New et Symbol par les polices PDF Type 1 de base en C#.
type: docs
weight: 310
url: /fr/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

Obtient ou définit une valeur déterminant s'il faut ou non remplacer les polices TrueType Arial, Times New Roman, Courier New et Symbol par les polices PDF Type 1 de base.

```csharp
public bool UseCoreFonts { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` . Lorsque cette valeur est fixée à`vrai` Les polices Arial, Times New Roman, Courier New et Symbol sont remplacées dans le document PDF par la police de base Type 1 correspondante.

Les polices PDF de base, ou leurs métriques de police et polices de substitution appropriées, doivent être disponibles pour toute application de visualisation PDF .

Ce paramètre fonctionne uniquement pour le texte en codage ANSI (Windows-1252). Le texte non ANSI sera write avec la police TrueType intégrée, quel que soit ce paramètre.

La conformité PDF/A et PDF/UA nécessite que toutes les polices soient intégrées.`FAUX` La valeur sera utilisée automatiquement lors de l'enregistrement au format PDF/A et PDF/UA.

Les polices principales ne sont pas prises en charge lors de l'enregistrement au format PDF 2.0.`FAUX` La valeur sera utilisée automatiquement lors de l'enregistrement au format PDF 2.0.

Cette option a une priorité plus élevée que[`FontEmbeddingMode`](../fontembeddingmode/) option.

## Exemples

Montre comment activer/désactiver la substitution de police PDF Type 1.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Fixe la propriété "UseCoreFonts" à "true" pour remplacer certaines polices,
// incluant les deux polices de notre document, avec leurs équivalents PDF Type 1.
// Définissez la propriété "UseCoreFonts" sur "false" pour ne pas appliquer les polices PDF Type 1.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);

if (useCoreFonts)
    Assert.That(3000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf").Length));
else
    Assert.That(30000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf").Length));
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
