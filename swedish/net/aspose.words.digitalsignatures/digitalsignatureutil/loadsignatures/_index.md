---
title: DigitalSignatureUtil.LoadSignatures
linktitle: LoadSignatures
articleTitle: LoadSignatures
second_title: Aspose.Words för .NET
description: Ladda enkelt digitala signaturer från dina dokument med DigitalSignatureUtil LoadSignatures-metoden. Förbättra ditt arbetsflöde idag!
type: docs
weight: 10
url: /sv/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(*string*) {#loadsignatures_1}

Laddar digitala signaturer från dokumentet.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Sökväg till dokumentet. |

### Returvärde

Samling av digitala signaturer. Returnerar en tom samling om filen inte är signerad.

## Exempel

Visar hur man laddar signaturer från ett digitalt signerat dokument.

```csharp
// Det finns två sätt att läsa in ett signerat dokuments samling av digitala signaturer med hjälp av klassen DigitalSignatureUtil.
// 1 - Ladda från ett dokument från ett lokalt filsystem filnamn:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Om den här samlingen inte är tom kan vi verifiera att dokumentet är digitalt signerat.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Ladda från ett dokument från en FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Visar hur man tar bort digitala signaturer från ett digitalt signerat dokument.

```csharp
// Det finns två sätt att använda DigitalSignatureUtil-klassen för att ta bort digitala signaturer
// från ett signerat dokument genom att spara en osignerad kopia av det någon annanstans i det lokala filsystemet.
// 1 - Bestäm platsen för både det signerade dokumentet och den osignerade kopian med hjälp av filnamnssträngar:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Bestäm platserna för både det signerade dokumentet och den osignerade kopian med hjälp av filströmmar:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verifiera att båda våra utdatadokument inte har några digitala signaturer.
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count);
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count);
```

### Se även

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)

---

## LoadSignatures(*Stream*) {#loadsignatures}

Laddar digitala signaturer från dokument med hjälp av ström.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Streama med dokumentet. |

### Returvärde

Samling av digitala signaturer. Returnerar en tom samling om filen inte är signerad.

## Exempel

Visar hur man laddar signaturer från ett digitalt signerat dokument.

```csharp
// Det finns två sätt att läsa in ett signerat dokuments samling av digitala signaturer med hjälp av klassen DigitalSignatureUtil.
// 1 - Ladda från ett dokument från ett lokalt filsystem filnamn:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Om den här samlingen inte är tom kan vi verifiera att dokumentet är digitalt signerat.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Ladda från ett dokument från en FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

### Se även

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
