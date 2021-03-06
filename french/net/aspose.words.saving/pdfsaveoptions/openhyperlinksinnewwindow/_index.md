---
title: OpenHyperlinksInNewWindow
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient ou définit une valeur déterminant si les hyperliens dans le document PDF de sortie sont forcés à souvrir dans une nouvelle fenêtre ou onglet dun navigateur.
type: docs
weight: 200
url: /fr/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Obtient ou définit une valeur déterminant si les hyperliens dans le document PDF de sortie sont forcés à s'ouvrir dans une nouvelle fenêtre (ou onglet) d'un navigateur.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

### Remarques

La valeur par défaut est`faux` . Lorsque cette valeur est définie sur`vrai` les hyperliens sont enregistrés à l'aide du code JavaScript. Le code JavaScript est`app.launchURL("URL", vrai);`, où`URL` est un lien hypertexte.

Notez que si cette option est définie sur`vrai` les hyperliens ne peuvent pas fonctionner dans certains lecteurs PDF, par exemple Chrome, Firefox.

Les actions JavaScript sont interdites par la conformité PDF/A-1 et PDF/A-2.`faux` sera utilisé automatiquement lorsque l'enregistrement au format PDF/A-1 et PDF/A-2.

### Exemples

Montre comment enregistrer des liens hypertexte dans un document que nous convertissons en PDF afin qu'ils ouvrent de nouvelles pages lorsque nous cliquons dessus.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", faux);

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "OpenHyperlinksInNewWindow" sur "true" pour enregistrer tous les hyperliens en utilisant le code Javascript
// qui oblige les lecteurs à ouvrir ces liens dans de nouvelles fenêtres/onglets de navigateur.
// Définissez la propriété "OpenHyperlinksInNewWindow" sur "false" pour enregistrer tous les hyperliens normalement.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../../pdfsaveoptions)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
