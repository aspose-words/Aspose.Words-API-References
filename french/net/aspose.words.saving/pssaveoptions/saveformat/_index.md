---
title: PsSaveOptions.SaveFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: PsSaveOptions propriété. Spécifie le format dans lequel le document sera enregistré si cet objet doptions de sauvegarde est utilisé. Ne peut êtrePs .
type: docs
weight: 20
url: /fr/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options de sauvegarde est utilisé. Ne peut êtrePs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Exemples

Montre comment enregistrer un document au format Postscript sous la forme d'un pli de livre.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Crée un objet "PsSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en PostScript.
// Définissez la propriété "UseBookFoldPrintingSettings" sur "true" pour organiser le contenu
// dans le document Postscript de sortie d'une manière qui nous aide à en faire un livret.
// Définissez la propriété "UseBookFoldPrintingSettings" sur "false" pour enregistrer le document normalement.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Si nous rendons le document sous forme de livret, nous devons définir les "MultiplePages"
// propriétés des objets de mise en page de toutes les sections à "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Une fois ce document imprimé recto verso, nous pouvons plier toutes les pages au milieu d'un coup,
// et le contenu s'alignera de manière à créer un livret.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pssaveoptions/)
* Assemblée [Aspose.Words](../../../)


