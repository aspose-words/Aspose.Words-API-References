---
title: FontFamily Enum
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Fonts.FontFamily, votre clé pour gérer sans effort diverses familles de polices pour un style et un formatage de document améliorés.
type: docs
weight: 3340
url: /fr/net/aspose.words.fonts/fontfamily/
---
## FontFamily enumeration

Représente la famille de polices.

```csharp
public enum FontFamily
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Auto | `0` | Spécifie un nom de famille générique. Ce nom est utilisé lorsque les informations sur une police sont inexistantes ou sans importance. La police par défaut est utilisée. |
| Roman | `1` | Spécifie une police proportionnelle avec empattements. Par exemple, Times New Roman. |
| Swiss | `2` | Spécifie une police proportionnelle sans empattements. Par exemple, Arial. |
| Modern | `3` | Spécifie une police à espacement fixe avec ou sans empattements. Les polices à espacement fixe sont généralement modernes ; par exemple, Pica, Elite et Courier New. |
| Script | `4` | Spécifie une police conçue pour ressembler à une écriture manuscrite ; les exemples incluent Script et Cursive. |
| Decorative | `5` | Spécifie une police originale. Par exemple, le vieil anglais. |

## Remarques

Une famille de polices est un ensemble de polices ayant une largeur de trait et des caractéristiques d'empattement communes.

## Exemples

Montre comment accéder et imprimer les détails de chaque police dans un document.

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
