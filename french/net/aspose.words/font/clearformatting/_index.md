---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words pour .NET
description: Font ClearFormatting méthode. Réinitialise le formatage de police par défaut en C#.
type: docs
weight: 550
url: /fr/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Réinitialise le formatage de police par défaut.

```csharp
public void ClearFormatting()
```

## Remarques

Supprime tout le formatage de police spécifié explicitement sur l'objet à partir duquel [`Font`](../) a été obtenu, le formatage de la police sera donc hérité de le parent approprié.

## Exemples

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

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
