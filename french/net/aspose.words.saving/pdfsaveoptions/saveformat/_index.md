---
title: PdfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words pour .NET
description: PdfSaveOptions SaveFormat propriété. Spécifie le format dans lequel le document sera enregistré si cet objet doptions de sauvegarde est utilisé. Ne peut êtrePdf  en C#.
type: docs
weight: 280
url: /fr/net/aspose.words.saving/pdfsaveoptions/saveformat/
---
## PdfSaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options de sauvegarde est utilisé. Ne peut êtrePdf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Exemples

Montre comment limiter le niveau des titres qui apparaîtront dans le plan d'un document PDF enregistré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère des titres pouvant servir d'entrées de table des matières des niveaux 1, 2, puis 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Le document PDF de sortie contiendra un plan, qui est une table des matières répertoriant les titres dans le corps du document.
// Cliquer sur une entrée de ce plan nous amènera à l'emplacement de son en-tête respectif.
// Définissez la propriété "HeadingsOutlineLevels" sur "2" pour exclure du plan tous les titres dont les niveaux sont supérieurs à 2.
// Les deux derniers titres que nous avons insérés ci-dessus n'apparaîtront pas.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
