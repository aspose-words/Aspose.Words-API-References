---
title: DigitalSignatureUtil Class
linktitle: DigitalSignatureUtil
articleTitle: DigitalSignatureUtil
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.DigitalSignatures.DigitalSignatureUtil för att enkelt signera dokument med säkra digitala signaturer. Förbättra dokumentintegriteten idag!
type: docs
weight: 610
url: /sv/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Tillhandahåller metoder för att signera dokument.

För att lära dig mer, besök[Arbeta med digitala signaturer](https://docs.aspose.com/words/net/working-with-digital-signatures/) dokumentationsartikel.

```csharp
public static class DigitalSignatureUtil
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(*Stream*) | Laddar digitala signaturer från dokument med hjälp av ström. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(*string*) | Laddar digitala signaturer från dokumentet. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(*Stream, Stream*) | Tar bort alla digitala signaturer från dokumentet i källströmmen och skriver osignerat dokument till destinationsströmmen. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(*string, string*) | Tar bort alla digitala signaturer från källfilen och skriver osignerad fil till destinationsfilen. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(*Stream, Stream, [CertificateHolder](../certificateholder/)*) | Signerar källdokument med hjälp av angivet[`CertificateHolder`](../certificateholder/) med digital signatur och skriver signerat dokument till destinationsströmmen. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(*string, string, [CertificateHolder](../certificateholder/)*) | Signerar källdokument med hjälp av angivet[`CertificateHolder`](../certificateholder/) med digital signatur och skriver signerat dokument till destinationsfilen. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(*Stream, Stream, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Signerar källdokument med hjälp av angivet[`CertificateHolder`](../certificateholder/) och[`SignOptions`](../signoptions/) med digital signatur och skriver signerat dokument till destinationsströmmen. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(*string, string, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Signerar källdokument med hjälp av angivet[`CertificateHolder`](../certificateholder/) och[`SignOptions`](../signoptions/) med digital signatur och skriver signerat dokument till destinationsfilen. |

## Anmärkningar

Eftersom digitala signaturer arbetar med filinnehåll snarare än dokumentobjektmodellen placeras dessa metoder i en separat klass.

Format som stöds är: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

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

* namnutrymme [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../)
