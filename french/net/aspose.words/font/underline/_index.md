---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Soulignage de police pour personnaliser les styles de texte. Définissez et modifiez facilement les types de soulignement pour une typographie améliorée dans vos créations.
type: docs
weight: 540
url: /fr/net/aspose.words/font/underline/
---
## Font.Underline property

Obtient ou définit le type de soulignement appliqué à la police.

```csharp
public Underline Underline { get; set; }
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

Montre comment insérer du texte formaté à l'aide de DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Spécifiez le formatage de la police, puis ajoutez du texte.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

Montre comment insérer un champ d'hyperlien.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Insérez un lien hypertexte et mettez-le en valeur avec une mise en forme personnalisée.
// L'hyperlien sera un morceau de texte cliquable qui nous mènera à l'emplacement spécifié dans l'URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", faux);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + clic gauche sur le lien dans le texte dans Microsoft Word nous amènera à l'URL via une nouvelle fenêtre de navigateur Web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Voir également

* enum [Underline](../../underline/)
* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
