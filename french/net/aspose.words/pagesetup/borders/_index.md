---
title: PageSetup.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Bordures de PageSetup pour accéder et personnaliser facilement les bordures de votre page pour un aspect soigné et professionnel dans vos documents.
type: docs
weight: 50
url: /fr/net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

Obtient une collection des bordures de page.

```csharp
public BorderCollection Borders { get; }
```

## Exemples

Montre comment créer une bordure de page ondulée verte avec une ombre.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Voir également

* class [BorderCollection](../../bordercollection/)
* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
