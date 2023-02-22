---
title: OdtSaveOptions.OdtSaveOptions
second_title: Aspose.Words för .NET API Referens
description: OdtSaveOptions byggare. Initierar en ny instans av denna klass som kan användas för att spara ett dokument iOdt format.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions() {#constructor}

Initierar en ny instans av denna klass som kan användas för att spara ett dokument iOdt format.

```csharp
public OdtSaveOptions()
```

### Exempel

Visar hur man får ett sparat dokument att överensstämma med ett äldre ODT-schema.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Se även

* class [OdtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../odtsaveoptions/)
* hopsättning [Aspose.Words](../../../)

---

## OdtSaveOptions(string) {#constructor_2}

Initierar en ny instans av denna klass som kan användas för att spara ett dokument iOdt format krypterad med ett lösenord.

```csharp
public OdtSaveOptions(string password)
```

### Se även

* class [OdtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../odtsaveoptions/)
* hopsättning [Aspose.Words](../../../)

---

## OdtSaveOptions(SaveFormat) {#constructor_1}

Initierar en ny instans av denna klass som kan användas för att spara ett dokument iOdt or Ott format.

```csharp
public OdtSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | SaveFormat | Kan varaOdt ellerOtt. |

### Exempel

Visar hur man krypterar ett sparat ODT/OTT-dokument med ett lösenord och sedan laddar det med Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Skapa ett nytt OdtSaveOptions och skicka antingen "SaveFormat.Odt",
// eller "SaveFormat.Ott" som formatet att spara dokumentet i. 
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Om vi öppnar det här dokumentet med en lämplig redigerare,
// det kommer att fråga oss om lösenordet vi angav i SaveOptions-objektet.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// Om vi vill öppna eller redigera detta dokument igen med Aspose.Words,
// vi måste tillhandahålla ett LoadOptions-objekt med rätt lösenord till laddningskonstruktorn.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../odtsaveoptions/)
* hopsättning [Aspose.Words](../../../)


