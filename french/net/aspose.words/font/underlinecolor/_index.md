---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font UnderlineColor pour personnaliser facilement la couleur de soulignement de votre police pour un style de texte amélioré et un attrait visuel.
type: docs
weight: 550
url: /fr/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Obtient ou définit la couleur du soulignement appliqué à la police.

```csharp
public Color UnderlineColor { get; set; }
```

## Exemples

Montre comment configurer le style et la couleur d'un soulignement de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
