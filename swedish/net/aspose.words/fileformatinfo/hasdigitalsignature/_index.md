---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FileFormatInfo HasDigitalSignature – kontrollera snabbt om ditt dokument innehåller en digital signatur, vilket förbättrar säkerheten och äktheten.
type: docs
weight: 20
url: /sv/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Returer`sann`om detta dokument innehåller en digital signatur. Den här egenskapen informerar bara om att en digital signatur finns på ett dokument, men den anger inte om signaturen är giltig eller inte.

```csharp
public bool HasDigitalSignature { get; }
```

## Anmärkningar

Den här egenskapen finns för att hjälpa dig sortera dokument som är digitalt signerade från de som inte är det. Om du använder Aspose.Words för att ändra och spara ett dokument som är digitalt signerat, kommer den digitala signaturen att gå förlorad. Detta är avsiktligt eftersom en digital signatur finns för att skydda ett dokuments äkthet. Med hjälp av den här egenskapen kan du identifiera digitalt signerade dokument innan du bearbetar dem på samma sätt som vanliga dokument och vidta åtgärder för att undvika att förlora den digitala signaturen, till exempel meddela användaren.

## Exempel

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

* class [FileFormatInfo](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
