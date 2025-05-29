---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IsTrueType de FontInfo, garantissant que votre police est TrueType ou OpenType pour une qualité supérieure, parfaite pour des conceptions nettes et évolutives.
type: docs
weight: 50
url: /fr/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Indique que cette police est une police TrueType ou OpenType, par opposition à une police raster ou vectorielle. La valeur par défaut est`vrai` .

```csharp
public bool IsTrueType { get; set; }
```

## Exemples

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

* class [FontInfo](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
