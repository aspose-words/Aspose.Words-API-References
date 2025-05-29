---
title: DocumentBuilder.MoveToHeaderFooter
linktitle: MoveToHeaderFooter
articleTitle: MoveToHeaderFooter
second_title: Aspose.Words pour .NET
description: Naviguez sans effort vers les en-têtes et les pieds de page avec la méthode MoveToHeaderFooter de DocumentBuilder, améliorant ainsi l'efficacité de l'édition de vos documents.
type: docs
weight: 580
url: /fr/net/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder.MoveToHeaderFooter method

Déplace le curseur au début d'un en-tête ou d'un pied de page dans la section actuelle.

```csharp
public void MoveToHeaderFooter(HeaderFooterType headerFooterType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | Spécifie l'en-tête ou le pied de page vers lequel se déplacer. |

## Remarques

Après avoir déplacé le curseur dans un en-tête ou un pied de page, vous pouvez utiliser le reste de[`DocumentBuilder`](../) méthodes pour modifier le contenu de l'en-tête ou du pied de page.

Si vous souhaitez créer des en-têtes et des pieds de page différents pour la première page, vous devez définir [`DifferentFirstPageHeaderFooter`](../../pagesetup/differentfirstpageheaderfooter/).

Si vous souhaitez créer des en-têtes et des pieds de page différents pour les pages paires et impaires, vous devez définir [`OddAndEvenPagesHeaderFooter`](../../pagesetup/oddandevenpagesheaderfooter/).

Utiliser[`MoveToSection`](../movetosection/) pour sortir de l'en-tête et accéder au texte principal.

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

Montre comment créer des en-têtes et des pieds de page dans un document à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez que nous voulons des en-têtes et des pieds de page différents pour les premières pages, les pages paires et les pages impaires.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Créez les en-têtes, puis ajoutez trois pages au document pour afficher chaque type d'en-tête.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Voir également

* enum [HeaderFooterType](../../headerfootertype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
