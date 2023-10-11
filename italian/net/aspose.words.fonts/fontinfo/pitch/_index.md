---
title: FontInfo.Pitch
second_title: Aspose.Words per .NET API Reference
description: FontInfo proprietà. Il passo indica se il carattere ha passo fisso spaziatura proporzionale o si basa su unimpostazione predefinita.
type: docs
weight: 70
url: /it/net/aspose.words.fonts/fontinfo/pitch/
---
## FontInfo.Pitch property

Il passo indica se il carattere ha passo fisso, spaziatura proporzionale o si basa su un'impostazione predefinita.

```csharp
public FontPitch Pitch { get; set; }
```

### Esempi

Mostra come accedere e stampare i dettagli di ciascun carattere in un documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // I nomi alternativi sono generalmente vuoti.
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

### Guarda anche

* enum [FontPitch](../../fontpitch/)
* class [FontInfo](../)
* spazio dei nomi [Aspose.Words.Fonts](../../fontinfo/)
* assemblea [Aspose.Words](../../../)


