---
title: FontInfo.Name
second_title: Référence de l'API Aspose.Words pour .NET
description: FontInfo propriété. Obtient le nom de la police.
type: docs
weight: 50
url: /fr/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Obtient le nom de la police.

```csharp
public string Name { get; }
```

### Remarques

C'est pas possible`nul`. Peut être une chaîne vide.

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


