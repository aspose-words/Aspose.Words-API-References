---
title: DigitalSignatureUtil.RemoveAllSignatures
linktitle: RemoveAllSignatures
articleTitle: RemoveAllSignatures
second_title: Aspose.Words för .NET
description: Ta enkelt bort alla digitala signaturer med DigitalSignatureUtils metod RemoveAllSignatures. Förvandla enkelt dina signerade filer till rena, osignerade versioner!
type: docs
weight: 20
url: /sv/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(*string, string*) {#removeallsignatures_1}

Tar bort alla digitala signaturer från källfilen och skriver osignerad fil till destinationsfilen.

Följande format är kompatibla för borttagning av digitala signaturer: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## Exempel

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

* class [DigitalSignatureUtil](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)

---

## RemoveAllSignatures(*Stream, Stream*) {#removeallsignatures}

Tar bort alla digitala signaturer från dokumentet i källströmmen och skriver osignerat dokument till destinationsströmmen.

**Utdata kommer att skrivas till början av strömmen och strömstorleken kommer att uppdateras med innehållets längd.**

Följande format är kompatibla för borttagning av digitala signaturer: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## Exempel

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

* class [DigitalSignatureUtil](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
