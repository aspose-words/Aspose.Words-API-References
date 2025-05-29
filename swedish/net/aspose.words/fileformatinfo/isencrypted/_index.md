---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: Aspose.Words för .NET
description: Ta reda på om ditt dokument är säkert med egenskapen FileFormatInfo IsEncrypted – returnerar sant för krypterade filer som kräver ett lösenord för åtkomst.
type: docs
weight: 40
url: /sv/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Returer`sann` om dokumentet är krypterat och kräver ett lösenord för att öppnas.

```csharp
public bool IsEncrypted { get; }
```

## Anmärkningar

Den här egenskapen finns för att hjälpa dig sortera dokument som är krypterade från de som inte är det. Om du försöker läsa in ett krypterat dokument med Aspose.Words utan att ange ett lösenord kommer ett -undantag att utlösas. Du kan använda den här egenskapen för att upptäcka om ett dokument kräver ett password och vidta åtgärder innan du laddar ett dokument, till exempel be användaren om ett lösenord.

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

### Se även

* class [FileFormatInfo](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
