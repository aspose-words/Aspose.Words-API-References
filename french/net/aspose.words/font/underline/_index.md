---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words pour .NET
description: Font Underline propriété. Obtient ou définit le type de soulignement appliqué à la police en C#.
type: docs
weight: 530
url: /fr/net/aspose.words/font/underline/
---
## Font.Underline property

Obtient ou définit le type de soulignement appliqué à la police.

```csharp
public Underline Underline { get; set; }
```

## Exemples

Montre comment configurer le style et la couleur du soulignement d’un texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

Montre comment insérer du texte formaté à l’aide de DocumentBuilder.

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

Montre comment insérer un champ de lien hypertexte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Insère un lien hypertexte et soulignez-le avec un formatage personnalisé.
// Le lien hypertexte sera un morceau de texte cliquable qui nous amènera à l'emplacement spécifié dans l'URL.
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
