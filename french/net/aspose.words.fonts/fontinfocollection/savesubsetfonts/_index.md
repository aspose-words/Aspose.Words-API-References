---
title: FontInfoCollection.SaveSubsetFonts
linktitle: SaveSubsetFonts
articleTitle: SaveSubsetFonts
second_title: Aspose.Words pour .NET
description: FontInfoCollection SaveSubsetFonts propriété. Spécifie sil faut ou non enregistrer un sousensemble des polices TrueType incorporées avec le document. La valeur par défaut de cette propriété estFAUX en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Spécifie s'il faut ou non enregistrer un sous-ensemble des polices TrueType incorporées avec le document. La valeur par défaut de cette propriété est`FAUX`.

Cette option ne fonctionne que lorsque[`EmbedTrueTypeFonts`](../embedtruetypefonts/) la propriété est définie sur`vrai`.

```csharp
public bool SaveSubsetFonts { get; set; }
```

## Remarques

Cette option fonctionne uniquement pour les formats DOC, DOCX et RTF.

## Exemples

Montre comment enregistrer un document avec des polices TrueType intégrées.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### Voir également

* class [FontInfoCollection](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
