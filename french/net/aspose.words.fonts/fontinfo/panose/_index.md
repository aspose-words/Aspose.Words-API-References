---
title: FontInfo.Panose
second_title: Référence de l'API Aspose.Words pour .NET
description: FontInfo propriété. Obtient ou définit le numéro de classification de la police de caractères PANOSE.
type: docs
weight: 60
url: /fr/net/aspose.words.fonts/fontinfo/panose/
---
## FontInfo.Panose property

Obtient ou définit le numéro de classification de la police de caractères PANOSE.

```csharp
public byte[] Panose { get; set; }
```

### Remarques

PANOSE est une description compacte de 10 octets des caractéristiques visuelles essentielles d'une police, telles que le contraste, l'épaisseur et le style serif. Les chiffres représentent le type de famille, le style Serif, le poids , la proportion, le contraste, la variation de trait, le style de bras, la forme de lettre, la ligne médiane et la hauteur X.

Peut être`nul`.

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

* class [FontInfo](../)
* espace de noms [Aspose.Words.Fonts](../../fontinfo/)
* Assemblée [Aspose.Words](../../../)


