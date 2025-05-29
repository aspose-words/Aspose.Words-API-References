---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words pour .NET
description: Contrôlez le comportement des hyperliens dans votre PDF avec PdfSaveOptions. Configurez facilement les liens pour qu'ils s'ouvrent dans une nouvelle fenêtre ou un nouvel onglet pour une expérience utilisateur améliorée.
type: docs
weight: 230
url: /fr/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Obtient ou définit une valeur déterminant si les hyperliens dans le document PDF de sortie doivent être forcés à être ouverts dans une nouvelle fenêtre (ou onglet) d'un navigateur.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` . Lorsque cette valeur est définie sur`vrai` Les hyperliens sont enregistrés à l'aide du code JavaScript. Le code JavaScript est`app.launchURL("URL", vrai);` , où`URL` est un hyperlien.

Notez que si cette option est définie sur`vrai` les hyperliens ne peuvent pas fonctionner dans certains lecteurs PDF, par exemple Chrome, Firefox.

Les actions JavaScript sont interdites par la conformité PDF/A-1 et PDF/A-2.`FAUX`sera utilisé automatiquement lors de l'enregistrement au format PDF/A-1 et PDF/A-2.

## Exemples

Montre comment enregistrer des hyperliens dans un document que nous convertissons en PDF afin qu'ils ouvrent de nouvelles pages lorsque nous cliquons dessus.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété « OpenHyperlinksInNewWindow » sur « true » pour enregistrer tous les hyperliens à l'aide du code Javascript
// qui oblige les lecteurs à ouvrir ces liens dans de nouvelles fenêtres/onglets de navigateur.
// Définissez la propriété « OpenHyperlinksInNewWindow » sur « false » pour enregistrer tous les hyperliens normalement.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
