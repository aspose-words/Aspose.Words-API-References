---
title: FontInfo.Panose
linktitle: Panose
articleTitle: Panose
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FontInfo PANOSE, obtenez ou définissez facilement le numéro de classification des polices pour une gestion améliorée des polices et une précision de conception.
type: docs
weight: 70
url: /fr/net/aspose.words.fonts/fontinfo/panose/
---
## FontInfo.Panose property

Obtient ou définit le numéro de classification de la police PANOSE.

```csharp
public byte[] Panose { get; set; }
```

## Remarques

PANOSE est une description compacte de 10 octets des caractéristiques visuelles essentielles d'une police, telles que le contraste, la graisse et le style d'empattement. Les chiffres représentent le type de police, le style d'empattement, la graisse, la proportion, le contraste, la variation de trait, le style de manche, la forme de lettre, la ligne médiane et la hauteur d'axe.

Peut être`nul`.

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

* class [FontInfo](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
