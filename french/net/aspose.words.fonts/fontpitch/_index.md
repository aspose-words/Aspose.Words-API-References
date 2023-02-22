---
title: Enum FontPitch
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fonts.FontPitch énumération. Représente le pas de la police.
type: docs
weight: 2780
url: /fr/net/aspose.words.fonts/fontpitch/
---
## FontPitch enumeration

Représente le pas de la police.

```csharp
public enum FontPitch
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Default | `0` | Spécifie qu'aucune information n'est disponible sur le pas d'une police. |
| Fixed | `1` | Spécifie qu'il s'agit d'une police à largeur fixe. |
| Variable | `2` | Spécifie qu'il s'agit d'une police à largeur proportionnelle. |

### Remarques

Le pas indique si la police est à pas fixe, espacée proportionnellement ou s'appuie sur un paramètre par défaut.

### Exemples

Montre comment accéder aux détails de chaque police dans un document et les imprimer.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // Les noms alternatifs sont généralement vides.
        Console.WriteLine("Alt name: " + fontInfo.AltName);
        Console.WriteLine("\t- Family: " + fontInfo.Family);
        Console.WriteLine("\t- " + (fontInfo.IsTrueType ? "Is TrueType" : "Is not TrueType"));
        Console.WriteLine("\t- Pitch: " + fontInfo.Pitch);
        Console.WriteLine("\t- Charset: " + fontInfo.Charset);
        Console.WriteLine("\t- Panose:");
        Console.WriteLine("\t\tFamily Kind: " + fontInfo.Panose[0]);
        Console.WriteLine("\t\tSerif Style: " + fontInfo.Panose[1]);
        Console.WriteLine("\t\tWeight: " + fontInfo.Panose[2]);
        Console.WriteLine("\t\tProportion: " + fontInfo.Panose[3]);
        Console.WriteLine("\t\tContrast: " + fontInfo.Panose[4]);
        Console.WriteLine("\t\tStroke Variation: " + fontInfo.Panose[5]);
        Console.WriteLine("\t\tArm Style: " + fontInfo.Panose[6]);
        Console.WriteLine("\t\tLetterform: " + fontInfo.Panose[7]);
        Console.WriteLine("\t\tMidline: " + fontInfo.Panose[8]);
        Console.WriteLine("\t\tX-Height: " + fontInfo.Panose[9]);
    }
}
```

### Voir également

* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)


