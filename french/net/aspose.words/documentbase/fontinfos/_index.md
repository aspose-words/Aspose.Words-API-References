---
title: DocumentBase.FontInfos
linktitle: FontInfos
articleTitle: FontInfos
second_title: Aspose.Words pour .NET
description: DocumentBase FontInfos propriété. Fournit un accès aux propriétés des polices utilisées dans ce document en C#.
type: docs
weight: 30
url: /fr/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

Fournit un accès aux propriétés des polices utilisées dans ce document.

```csharp
public FontInfoCollection FontInfos { get; }
```

## Remarques

Cette collection de définitions de polices est chargée telle quelle à partir du document. Les définitions de polices peuvent être facultatives, manquantes ou incomplètes dans certains documents.

Ne vous fiez pas à cette collection pour vérifier qu'une police particulière est utilisée dans le document. Vous ne devez utiliser cette collection que pour obtenir des informations sur les polices susceptibles d'être utilisées dans le document.

## Exemples

Montre comment imprimer les détails des polices présentes dans un document.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Imprime toutes les polices utilisées et inutilisées dans le document.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

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

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
