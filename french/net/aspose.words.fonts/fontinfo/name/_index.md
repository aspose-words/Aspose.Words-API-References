---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FontInfo Name pour accéder et utiliser facilement les noms de polices pour une typographie améliorée dans vos projets.
type: docs
weight: 60
url: /fr/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Obtient le nom de la police.

```csharp
public string Name { get; }
```

## Remarques

Ne peut pas être`nul`. Peut être une chaîne vide.

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
