---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words pour .NET
description: Optimisez la mise en page de votre document avec la propriété XpsSaveOptions UseBookFoldPrintingSettings, permettant une impression de livret transparente pour une présentation améliorée.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré à l'aide d'une mise en page d'impression de livret, si elle est spécifiée via[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Remarques

Si cette option est spécifiée,[`PageSet`](../../fixedpagesaveoptions/pageset/) est ignoré lors de l'enregistrement. Ce comportement correspond à MS Word. Si les paramètres d'impression de pliage de livre ne sont pas spécifiés dans la mise en page, cette option n'aura aucun effet.

## Exemples

Montre comment enregistrer un document au format XPS sous la forme d'un pli de livre.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Créez un objet « XpsSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Définissez la propriété « UseBookFoldPrintingSettings » sur « true » pour organiser le contenu
// dans le XPS de sortie d'une manière qui nous aide à l'utiliser pour créer un livret.
// Définissez la propriété « UseBookFoldPrintingSettings » sur « false » pour restituer le XPS normalement.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Si nous rendons le document sous forme de livret, nous devons définir les « MultiplePages »
// propriétés des objets de mise en page de toutes les sections sur « MultiplePagesType.BookFoldPrinting ».
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Une fois ce document imprimé, nous pouvons le transformer en livret en empilant les pages
// pour sortir de l'imprimante et plier au milieu.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Voir également

* class [XpsSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
