---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup TextOrientation pour définir facilement l'orientation du texte. Personnalisez votre mise en page avec des options allant au-delà de l'orientation horizontale par défaut.
type: docs
weight: 430
url: /fr/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Permet de spécifier`TextOrientation` pour toute la page. La valeur par défaut estHorizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## Remarques

Cette propriété est uniquement prise en charge pour les formats natifs MS Word DOCX, WML, RTF et DOC.

## Exemples

Montre comment définir l'orientation du texte.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Définissez la propriété « TextOrientation » sur « TextOrientation.Upward » pour faire pivoter tout le texte de 90 degrés
// vers la droite pour que tout le texte de gauche à droite aille désormais de haut en bas.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Voir également

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
