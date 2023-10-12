---
title: LayoutOptions.ShowHiddenText
second_title: Référence de l'API Aspose.Words pour .NET
description: LayoutOptions propriété. Obtient ou définit une indication indiquant si le texte masqué dans le document est rendu. La valeur par défaut estFAUX .
type: docs
weight: 80
url: /fr/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Obtient ou définit une indication indiquant si le texte masqué dans le document est rendu. La valeur par défaut est`FAUX` .

```csharp
public bool ShowHiddenText { get; set; }
```

### Remarques

Cette propriété affecte tout le contenu masqué, pas seulement le texte.

### Exemples

Montre comment masquer le texte dans un document de sortie rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Insère du texte masqué, puis précise si nous souhaitons l'omettre d'un document rendu.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### Voir également

* class [LayoutOptions](../)
* espace de noms [Aspose.Words.Layout](../../layoutoptions/)
* Assemblée [Aspose.Words](../../../)


