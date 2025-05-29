---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fonts.FontInfoCollection, votre solution de référence pour gérer efficacement les polices de documents et améliorer l'attrait visuel de votre document.
type: docs
weight: 3360
url: /fr/net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

Représente une collection de polices utilisées dans un document.

Pour en savoir plus, visitez le[Travailler avec les polices](https://docs.aspose.com/words/net/working-with-fonts/) article de documentation.

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | Spécifie s'il faut ou non incorporer les polices système dans le document. La valeur par défaut de cette propriété est`FAUX`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | Spécifie s'il faut ou non incorporer les polices TrueType dans un document lors de son enregistrement. La valeur par défaut de cette propriété est`FAUX` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | Obtient une police avec le nom spécifié. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | Spécifie s'il faut ou non enregistrer un sous-ensemble des polices TrueType incorporées avec le document. La valeur par défaut de cette propriété est`FAUX`. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | Détermine si la collection contient une police avec le nom donné. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |

## Remarques

Les articles sont[`FontInfo`](../fontinfo/) objets.

Vous ne créez pas d'instances de cette classe directement. Utilisez le[`FontInfos`](../../aspose.words/documentbase/fontinfos/) propriété permettant d'accéder à la collection de polices définie dans le document.

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

Montre comment imprimer les détails des polices présentes dans un document.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Imprimez toutes les polices utilisées et non utilisées dans le document.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Voir également

* class [FontInfo](../fontinfo/)
* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
