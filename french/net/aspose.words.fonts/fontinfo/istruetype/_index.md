---
title: FontInfo.IsTrueType
second_title: Référence de l'API Aspose.Words pour .NET
description: FontInfo propriété. Indique que cette police est une police TrueType ou OpenType par opposition à une police raster ou vectorielle. La valeur par défaut estvrai .
type: docs
weight: 40
url: /fr/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Indique que cette police est une police TrueType ou OpenType par opposition à une police raster ou vectorielle. La valeur par défaut est`vrai` .

```csharp
public bool IsTrueType { get; set; }
```

### Exemples

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

### Voir également

* class [FontInfo](../)
* espace de noms [Aspose.Words.Fonts](../../fontinfo/)
* Assemblée [Aspose.Words](../../../)


