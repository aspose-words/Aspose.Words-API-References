---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété FontInfoCollection EmbedSystemFonts améliore vos documents en intégrant les polices système. Découvrez sa valeur par défaut et ses avantages !
type: docs
weight: 20
url: /fr/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Spécifie s'il faut ou non incorporer les polices système dans le document. La valeur par défaut de cette propriété est`FAUX`.

Cette option ne fonctionne que lorsque[`EmbedTrueTypeFonts`](../embedtruetypefonts/) l'option est définie sur`vrai`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## Remarques

Définition de cette propriété sur`vrai` Ceci est utile si l'utilisateur utilise un système d'Asie de l'Est et souhaite créer un document lisible par d'autres utilisateurs ne disposant pas de polices pour cette langue. Par exemple, un utilisateur utilisant un système japonais pourrait choisir d'intégrer les polices dans un document afin que celui-ci soit lisible sur tous les systèmes.

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
