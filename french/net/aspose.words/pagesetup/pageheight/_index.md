---
title: PageSetup.PageHeight
linktitle: PageHeight
articleTitle: PageHeight
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup PageHeight pour gérer efficacement la hauteur de votre document en points, améliorant ainsi votre mise en page et votre présentation.
type: docs
weight: 310
url: /fr/net/aspose.words/pagesetup/pageheight/
---
## PageSetup.PageHeight property

Renvoie ou définit la hauteur de la page en points.

```csharp
public double PageHeight { get; set; }
```

## Exemples

Montre comment insérer une image et l'utiliser comme filigrane.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez l'image dans l'en-tête afin qu'elle soit visible sur chaque page.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Placez l'image au centre de la page.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
