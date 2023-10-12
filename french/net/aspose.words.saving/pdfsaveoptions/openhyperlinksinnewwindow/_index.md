---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions propriété. Obtient ou définit une valeur déterminant si les hyperliens dans le document Pdf de sortie doivent être ouverts de force dans une nouvelle fenêtre ou onglet dun navigateur.
type: docs
weight: 230
url: /fr/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Obtient ou définit une valeur déterminant si les hyperliens dans le document Pdf de sortie doivent être ouverts de force dans une nouvelle fenêtre (ou onglet) d'un navigateur.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

### Remarques

La valeur par défaut est`FAUX` . Lorsque cette valeur est fixée à`vrai` Les hyperliens sont enregistrés à l'aide du code JavaScript. Le code JavaScript est`app.launchURL("URL", true);` , où`URL` est un hyperlien.

Notez que si cette option est définie sur`vrai` les hyperliens ne peuvent pas fonctionner dans certains lecteurs PDF, par exemple Chrome, Firefox.

Les actions JavaScript sont interdites par la conformité PDF/A-1 et PDF/A-2.`FAUX`sera utilisé automatiquement lors de l'enregistrement au format PDF/A-1 et PDF/A-2.

### Exemples

Montre comment enregistrer des hyperliens dans un document que nous convertissons en PDF afin qu'ils ouvrent de nouvelles pages lorsque nous cliquons dessus.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "OpenHyperlinksInNewWindow" sur "true" pour enregistrer tous les hyperliens à l'aide du code Javascript
// qui oblige les lecteurs à ouvrir ces liens dans de nouveaux onglets de fenêtres/navigateur.
// Définissez la propriété "OpenHyperlinksInNewWindow" sur "false" pour enregistrer tous les hyperliens normalement.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


