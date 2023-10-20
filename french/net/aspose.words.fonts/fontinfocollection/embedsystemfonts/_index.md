---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words pour .NET
description: FontInfoCollection EmbedSystemFonts propriété. Spécifie sil faut ou non intégrer les polices système dans le document. La valeur par défaut de cette propriété estFAUX en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Spécifie s'il faut ou non intégrer les polices système dans le document. La valeur par défaut de cette propriété est`FAUX`.

Cette option ne fonctionne que lorsque[`EmbedTrueTypeFonts`](../embedtruetypefonts/) l'option est définie sur`vrai`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## Remarques

Définir cette propriété sur`vrai`est utile si l'utilisateur se trouve sur un système d'Asie de l'Est et souhaite créer un document lisible par d'autres personnes qui n'ont pas de polices pour cette langue sur leur système. Par exemple, un utilisateur sur un système japonais pourrait choisir d'incorporer les polices dans un document afin que le document japonais soit lisible sur tous les systèmes.

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
