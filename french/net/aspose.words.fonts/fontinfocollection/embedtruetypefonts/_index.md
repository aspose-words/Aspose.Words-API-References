---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété EmbedTrueTypeFonts de FontInfoCollection améliore la qualité du document en autorisant l'incorporation de polices TrueType. La valeur par défaut est « false ».
type: docs
weight: 30
url: /fr/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Spécifie s'il faut ou non incorporer les polices TrueType dans un document lors de son enregistrement. La valeur par défaut de cette propriété est`FAUX` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## Remarques

L'intégration de polices TrueType permet à d'autres personnes de visualiser le document avec les mêmes polices que celles utilisées pour le créer, mais peut augmenter considérablement la taille du document.

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
