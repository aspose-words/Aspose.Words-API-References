---
title: PlainTextDocument
second_title: Aspose.Words för .NET API Referens
description: Skapar ett vanligt textdokument från en fil. Upptäcker automatiskt filformatet.
type: docs
weight: 10
url: /sv/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(string) {#constructor_2}

Skapar ett vanligt textdokument från en fil. Upptäcker automatiskt filformatet.

```csharp
public PlainTextDocument(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namnet på filen att extrahera texten från. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception) | Dokumentet verkar vara skadat och kan inte laddas. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklare. |
| IOException | Det finns ett input/output undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du har angett ett felaktigt lösenord. |
| ArgumentException | Namnet på filen får inte vara null eller tom sträng. |

### Exempel

Visar hur man laddar innehållet i ett Microsoft Word-dokument i klartext.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Se även

* class [PlainTextDocument](../../plaintextdocument)
* namnutrymme [Aspose.Words](../../plaintextdocument)
* hopsättning [Aspose.Words](../../../)

---

## PlainTextDocument(string, LoadOptions) {#constructor_3}

Skapar ett vanligt textdokument från en fil. Tillåter att ange ytterligare alternativ såsom ett krypteringslösenord.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namnet på filen att extrahera texten från. |
| loadOptions | LoadOptions | Ytterligare alternativ att använda när du laddar ett dokument. Kan vara null. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception) | Dokumentet verkar vara skadat och kan inte laddas. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklare. |
| IOException | Det finns ett input/output undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du har angett ett felaktigt lösenord. |
| ArgumentException | Namnet på filen får inte vara null eller tom sträng. |

### Exempel

Visar hur man laddar innehållet i ett krypterat Microsoft Word-dokument i klartext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", loadOptions);

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Se även

* class [LoadOptions](../../../aspose.words.loading/loadoptions)
* class [PlainTextDocument](../../plaintextdocument)
* namnutrymme [Aspose.Words](../../plaintextdocument)
* hopsättning [Aspose.Words](../../../)

---

## PlainTextDocument(Stream) {#constructor}

Skapar ett vanligt textdokument från en ström. Upptäcker automatiskt filformatet.

```csharp
public PlainTextDocument(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen varifrån texten ska extraheras. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception) | Dokumentet verkar vara skadat och kan inte laddas. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklare. |
| IOException | Det finns ett input/output undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du har angett ett felaktigt lösenord. |
| ArgumentNullException | Strömmen kan inte vara null. |
| NotSupportedException | Strömmen stöder inte läsning eller sökning. |
| ObjectDisposedException | Strömmen är ett kasserat föremål. |

### Anmärkningar

Dokumentet måste lagras i början av streamen. Strömmen måste stödja slumpmässig positionering.

### Exempel

Visar hur man laddar innehållet i ett Microsoft Word-dokument i klartext med stream.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx");

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Se även

* class [PlainTextDocument](../../plaintextdocument)
* namnutrymme [Aspose.Words](../../plaintextdocument)
* hopsättning [Aspose.Words](../../../)

---

## PlainTextDocument(Stream, LoadOptions) {#constructor_1}

Skapar ett vanligt textdokument från en ström. Tillåter att ange ytterligare alternativ såsom ett krypteringslösenord.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen varifrån texten ska extraheras. |
| loadOptions | LoadOptions | Ytterligare alternativ att använda när du laddar ett dokument. Kan vara null. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception) | Dokumentet verkar vara skadat och kan inte laddas. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklare. |
| IOException | Det finns ett input/output undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du har angett ett felaktigt lösenord. |
| ArgumentNullException | Strömmen kan inte vara null. |
| NotSupportedException | Strömmen stöder inte läsning eller sökning. |
| ObjectDisposedException | Strömmen är ett kasserat föremål. |

### Anmärkningar

Dokumentet måste lagras i början av streamen. Strömmen måste stödja slumpmässig positionering.

### Exempel

Visar hur man laddar innehållet i ett krypterat Microsoft Word-dokument i klartext med stream.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream, loadOptions);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Se även

* class [LoadOptions](../../../aspose.words.loading/loadoptions)
* class [PlainTextDocument](../../plaintextdocument)
* namnutrymme [Aspose.Words](../../plaintextdocument)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
