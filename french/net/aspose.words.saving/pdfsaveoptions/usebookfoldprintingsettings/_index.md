---
title: PdfSaveOptions.UseBookFoldPrintingSettings
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions propriété. Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré à laide dune mise en page dimpression en livret sil est spécifié viaMultiplePages .
type: docs
weight: 300
url: /fr/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré à l'aide d'une mise en page d'impression en livret, s'il est spécifié via[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### Remarques

Si cette option est spécifiée,[`PageSet`](../../fixedpagesaveoptions/pageset/) est ignoré lors de l'enregistrement. Ce comportement correspond à MS Word. Si les paramètres d'impression du pli du livre ne sont pas spécifiés dans la mise en page, cette option n'aura aucun effet.

### Exemples

Montre comment enregistrer un document au format PDF sous la forme d'un pli de livre.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "UseBookFoldPrintingSettings" sur "true" pour organiser le contenu
// dans le PDF de sortie d'une manière qui nous aide à l'utiliser pour créer un livret.
// Définissez la propriété "UseBookFoldPrintingSettings" sur "false" pour rendre le PDF normalement.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Si nous rendons le document sous forme de livret, nous devons définir les "MultiplePages"
// propriétés des objets de mise en page de toutes les sections à "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Une fois ce document imprimé recto verso, nous pouvons plier toutes les pages au milieu d'un coup,
// et le contenu s'alignera de manière à créer un livret.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


