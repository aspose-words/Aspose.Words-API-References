---
title: FontInfoCollection.GetEnumerator
second_title: Référence de l'API Aspose.Words pour .NET
description: FontInfoCollection méthode. Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection.
type: docs
weight: 70
url: /fr/net/aspose.words.fonts/fontinfocollection/getenumerator/
---
## FontInfoCollection.GetEnumerator method

Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection.

```csharp
public IEnumerator<FontInfo> GetEnumerator()
```

### Exemples

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

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* espace de noms [Aspose.Words.Fonts](../../fontinfocollection/)
* Assemblée [Aspose.Words](../../../)


