---
title: DigitalSignatureUtil.RemoveAllSignatures
linktitle: RemoveAllSignatures
articleTitle: RemoveAllSignatures
second_title: Aspose.Words för .NET
description: DigitalSignatureUtil RemoveAllSignatures metod. Tar bort alla digitala signaturer från källfilen och skriver osignerad fil till målfilen i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(*string, string*) {#removeallsignatures_1}

Tar bort alla digitala signaturer från källfilen och skriver osignerad fil till målfilen.

Följande format är kompatibla för borttagning av digital signatur: Doc , Dot , Docx , Dotx , Docm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## Exempel

Visar hur du tar bort digitala signaturer från ett digitalt signerat dokument.

```csharp
// Det finns två sätt att använda klassen DigitalSignatureUtil för att ta bort digitala signaturer
// från ett signerat dokument genom att spara en osignerad kopia av det någon annanstans i det lokala filsystemet.
// 1 - Bestäm platserna för både det signerade dokumentet och den osignerade kopian med filnamnssträngar:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Bestäm platserna för både det signerade dokumentet och den osignerade kopian av filströmmar:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verifiera att båda våra utdatadokument inte har några digitala signaturer.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### Se även

* class [DigitalSignatureUtil](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)

---

## RemoveAllSignatures(*Stream, Stream*) {#removeallsignatures}

Tar bort alla digitala signaturer från dokumentet i källströmmen och skriver osignerat dokument till målströmmen.

**Utdata kommer att skrivas till starten av strömmen och strömstorleken kommer att uppdateras med innehållets längd.**

Följande format är kompatibla för borttagning av digital signatur: Doc , Dot , Docx , Dotx , Docm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## Exempel

Visar hur du tar bort digitala signaturer från ett digitalt signerat dokument.

```csharp
// Det finns två sätt att använda klassen DigitalSignatureUtil för att ta bort digitala signaturer
// från ett signerat dokument genom att spara en osignerad kopia av det någon annanstans i det lokala filsystemet.
// 1 - Bestäm platserna för både det signerade dokumentet och den osignerade kopian med filnamnssträngar:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Bestäm platserna för både det signerade dokumentet och den osignerade kopian av filströmmar:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verifiera att båda våra utdatadokument inte har några digitala signaturer.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### Se även

* class [DigitalSignatureUtil](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
