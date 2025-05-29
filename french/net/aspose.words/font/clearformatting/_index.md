---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words pour .NET
description: Restaurez le style d'origine de votre texte grâce à la méthode Font ClearFormatting. Profitez d'une mise en forme propre et cohérente pour un rendu soigné !
type: docs
weight: 560
url: /fr/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Réinitialise le formatage de police par défaut.

```csharp
public void ClearFormatting()
```

## Remarques

Supprime toute la mise en forme de police spécifiée explicitement sur l'objet à partir duquel [`Font`](../) a été obtenu afin que le formatage de la police soit hérité de le parent approprié.

## Exemples

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

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
