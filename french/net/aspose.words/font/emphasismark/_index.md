---
title: Font.EmphasisMark
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser la propriété Marque d'emphase de police pour améliorer la mise en forme de votre texte. Apprenez à définir et personnaliser les marques d'emphase pour une meilleure lisibilité.
type: docs
weight: 110
url: /fr/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

Obtient ou définit la marque d'emphase appliquée à cette mise en forme.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

## Exemples

Montre comment ajouter un caractère supplémentaire rendu au-dessus/en dessous du caractère glyphe.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Types possibles de marque d'emphase :
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### Voir également

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
