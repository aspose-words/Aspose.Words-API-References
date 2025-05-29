---
title: FileFormatInfo Class
linktitle: FileFormatInfo
articleTitle: FileFormatInfo
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.FileFormatInfo för effektiv identifiering av dokumentformat. Få tillgång till detaljerad data för att förbättra dina filhanteringslösningar.
type: docs
weight: 3220
url: /sv/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

Innehåller data som returneras av[`FileFormatUtil`](../fileformatutil/) metoder för dokumentformatdetektering.

För att lära dig mer, besök[Identifiera filformat och kontrollera formatkompatibilitet](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) dokumentationsartikel.

```csharp
public class FileFormatInfo
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Hämtar den detekterade kodningen om den är tillämplig för det aktuella dokumentformatet. För närvarande identifieras kodning endast för HTML-dokument. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | Returer`sann`om detta dokument innehåller en digital signatur. Den här egenskapen informerar bara om att en digital signatur finns på ett dokument, men den anger inte om signaturen är giltig eller inte. |
| [HasMacros](../../aspose.words/fileformatinfo/hasmacros/) { get; } | Returer`sann` om det här dokumentet innehåller VBA-makro. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | Returer`sann` om dokumentet är krypterat och kräver ett lösenord för att öppnas. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Hämtar det detekterade dokumentformatet. |

## Anmärkningar

Du skapar inte instanser av den här klassen direkt. Objekt i den här klassen returneras av [`DetectFileFormat`](../fileformatutil/detectfileformat/) metoder.

## Exempel

Visar hur man använder FileFormatUtil-klassen för att identifiera dokumentformat och kryptering.

```csharp
Document doc = new Document();

// Konfigurera ett SaveOptions-objekt för att kryptera dokumentet
// med ett lösenord när vi sparar det, och sedan sparar vi dokumentet.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verifiera filtypen för vårt dokument och dess krypteringsstatus.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

Visar hur man använder FileFormatUtil-klassen för att identifiera dokumentformat och förekomst av digitala signaturer.

```csharp
// Använd en FileFormatInfo-instans för att verifiera att ett dokument inte är digitalt signerat.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// Använd en ny FileFormatInstance för att bekräfta att den är signerad.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Vi kan ladda och komma åt signaturerna för ett signerat dokument i en samling som denna.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
