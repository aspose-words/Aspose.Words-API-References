---
title: FileFormatInfo.IsEncrypted
second_title: Aspose.Words för .NET API Referens
description: FileFormatInfo fast egendom. Returnerar sant om dokumentet är krypterat och kräver ett lösenord för att öppnas.
type: docs
weight: 30
url: /sv/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Returnerar sant om dokumentet är krypterat och kräver ett lösenord för att öppnas.

```csharp
public bool IsEncrypted { get; }
```

### Anmärkningar

Den här egenskapen finns för att hjälpa dig sortera dokument som är krypterade från de som inte är det. Om du försöker ladda ett krypterat dokument med Aspose.Words utan att ange ett lösenord kommer ett undantag att kastas. Du kan använda den här egenskapen för att upptäcka om ett dokument kräver ett lösenord och vidta några åtgärder innan du laddar ett dokument, till exempel fråga användaren om ett lösenord.

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

### Se även

* class [FileFormatInfo](../)
* namnutrymme [Aspose.Words](../../fileformatinfo/)
* hopsättning [Aspose.Words](../../../)


