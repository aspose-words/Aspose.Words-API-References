---
title: XpsSaveOptions.UseBookFoldPrintingSettings
second_title: Référence de l'API Aspose.Words pour .NET
description: XpsSaveOptions propriété. Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré à laide dune mise en page dimpression en livret sil est spécifié viaMultiplePages .
type: docs
weight: 40
url: /fr/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré à l'aide d'une mise en page d'impression en livret, s'il est spécifié via[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### Remarques

Si cette option est spécifiée,[`PageSet`](../../fixedpagesaveoptions/pageset/) est ignoré lors de l'enregistrement. Ce comportement correspond à MS Word. Si les paramètres d'impression du pli du livre ne sont pas spécifiés dans la mise en page, cette option n'aura aucun effet.

### Exemples

Montre comment enregistrer un document au format XPS sous la forme d'un pli de livre.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Crée un objet "XpsSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Définissez la propriété "UseBookFoldPrintingSettings" sur "true" pour organiser le contenu
// dans la sortie XPS d'une manière qui nous aide à l'utiliser pour créer un livret.
// Définissez la propriété "UseBookFoldPrintingSettings" sur "false" pour restituer le XPS normalement.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Si nous rendons le document sous forme de livret, nous devons définir les "MultiplePages"
// propriétés des objets de mise en page de toutes les sections à "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Une fois ce document imprimé, nous pouvons le transformer en livret en empilant les pages
// pour sortir de l'imprimante et replier au milieu.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Voir également

* class [XpsSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../xpssaveoptions/)
* Assemblée [Aspose.Words](../../../)


