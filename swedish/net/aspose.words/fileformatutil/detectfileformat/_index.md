---
title: DetectFileFormat
second_title: Aspose.Words för .NET API Referens
description: Upptäcker och returnerar information om formatet för ett dokument som lagras i en diskfil.
type: docs
weight: 30
url: /sv/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(string) {#detectfileformat_1}

Upptäcker och returnerar information om formatet för ett dokument som lagras i en diskfil.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Filnamnet. |

### Returvärde

A[`FileFormatInfo`](../../fileformatinfo) objekt som innehåller den upptäckta informationen.

### Anmärkningar

Även om den här metoden upptäcker dokumentformatet, garanterar den inte att det angivna dokumentet är giltigt. Denna metod upptäcker endast dokumentformatet genom att läsa data som är tillräckliga för upptäckt. För att fullständigt verifiera att ett dokument är giltigt måste du ladda dokumentet i en[`Document`](../../document) objekt.

Denna metod kastar[`FileCorruptedException`](../../filecorruptedexception) när formatet känns igen, men upptäckten kan inte slutföras på grund av korruption.

### Exempel

Visar hur du använder klassen FileFormatUtil för att upptäcka dokumentformat och kryptering.

```csharp
Document doc = new Document();

// Konfigurera ett SaveOptions-objekt för att kryptera dokumentet
// med ett lösenord när vi sparar det, och sedan spara dokumentet.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verifiera filtypen för vårt dokument och dess krypteringsstatus.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

Visar hur du använder klassen FileFormatUtil för att upptäcka dokumentformatet och förekomsten av digitala signaturer.

```csharp
// Använd en FileFormatInfo-instans för att verifiera att ett dokument inte är digitalt signerat.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// Använd en ny FileFormatInstance för att bekräfta att den är signerad.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Vi kan ladda och komma åt signaturerna för ett signerat dokument i en samling som denna.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Se även

* class [FileFormatInfo](../../fileformatinfo)
* class [FileFormatUtil](../../fileformatutil)
* namnutrymme [Aspose.Words](../../fileformatutil)
* hopsättning [Aspose.Words](../../../)

---

## DetectFileFormat(Stream) {#detectfileformat}

Upptäcker och returnerar information om formatet för ett dokument som lagras i en ström.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen. |

### Returvärde

A[`FileFormatInfo`](../../fileformatinfo) objekt som innehåller den upptäckta informationen.

### Anmärkningar

Strömmen måste placeras i början av dokumentet.

När denna metod återkommer återställs positionen i strömmen till den ursprungliga positionen.

Även om den här metoden upptäcker dokumentformatet, garanterar den inte att det angivna dokumentet är giltigt. Denna metod upptäcker endast dokumentformatet genom att läsa data som är tillräckliga för upptäckt. För att fullständigt verifiera att ett dokument är giltigt måste du ladda dokumentet i en[`Document`](../../document) objekt.

Denna metod kastar[`FileCorruptedException`](../../filecorruptedexception) när formatet känns igen, men upptäckten kan inte slutföras på grund av korruption.

### Exempel

Visar hur du använder FileFormatUtil-metoderna för att upptäcka formatet på ett dokument.

```csharp
// Ladda ett dokument från en fil som saknar filtillägg, och identifiera sedan dess filformat.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Nedan finns två metoder för att konvertera ett LoadFormat till dess motsvarande SaveFormat.
    // 1 - Hämta filtilläggssträngen för LoadFormat och hämta sedan motsvarande SaveFormat från den strängen:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Konvertera LoadFormat direkt till dess SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Ladda ett dokument från strömmen och spara det sedan i det automatiskt upptäckta filtillägget.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Se även

* class [FileFormatInfo](../../fileformatinfo)
* class [FileFormatUtil](../../fileformatutil)
* namnutrymme [Aspose.Words](../../fileformatutil)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
