---
title: FontInfoCollection.SaveSubsetFonts
linktitle: SaveSubsetFonts
articleTitle: SaveSubsetFonts
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SaveSubsetFonts de FontInfoCollection, contrôlez les sous-ensembles de polices TrueType intégrés dans vos documents pour une taille de fichier et des performances optimisées.
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
```

### Voir également

* class [FontInfoCollection](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
