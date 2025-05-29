---
title: LayoutOptions.ShowHiddenText
linktitle: ShowHiddenText
articleTitle: ShowHiddenText
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShowHiddenText de LayoutOptions pour contrôler facilement l'affichage du texte masqué dans vos documents. Optimisez la visibilité de votre contenu dès aujourd'hui !
type: docs
weight: 80
url: /fr/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Obtient ou définit une indication indiquant si le texte masqué dans le document est rendu. La valeur par défaut est`FAUX` .

```csharp
public bool ShowHiddenText { get; set; }
```

## Remarques

Cette propriété affecte tout le contenu caché, pas seulement le texte.

## Exemples

Montre comment masquer du texte dans un document de sortie rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Insérer du texte masqué, puis spécifier si nous souhaitons l'omettre d'un document rendu.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### Voir également

* class [LayoutOptions](../)
* espace de noms [Aspose.Words.Layout](../../../aspose.words.layout/)
* Assemblée [Aspose.Words](../../../)
