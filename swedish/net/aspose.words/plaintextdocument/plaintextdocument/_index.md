---
title: PlainTextDocument
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words för .NET
description: Skapa enkelt dokument i klartext med vår PlainTextDocument-konstruktor. Njut av automatisk filformatidentifiering för sömlös integration!
type: docs
weight: 10
url: /sv/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(*string*) {#constructor_2}

Skapar ett vanligt textdokument från en fil. Identifierar automatiskt filformatet.

```csharp
public PlainTextDocument(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namn på filen att extrahera texten från. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception/) | Dokumentet verkar vara skadat och kan inte läsas in. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklarna. |
| IOException | Det finns ett indata/utdata-undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du angav ett felaktigt lösenord. |
| ArgumentException | Filnamnet får inte vara null eller en tom sträng. |

## Exempel

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

* class [PlainTextDocument](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## PlainTextDocument(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_3}

Skapar ett vanligt textdokument från en fil. Gör det möjligt att ange ytterligare alternativ, till exempel ett krypteringslösenord.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namn på filen att extrahera texten från. |
| loadOptions | LoadOptions | Ytterligare alternativ att använda när du laddar ett dokument. Kan vara`null`. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception/) | Dokumentet verkar vara skadat och kan inte läsas in. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklarna. |
| IOException | Det finns ett indata/utdata-undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du angav ett felaktigt lösenord. |
| ArgumentException | Filnamnet får inte vara null eller en tom sträng. |

## Exempel

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

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream*) {#constructor}

Skapar ett vanligt textdokument från en ström. Identifierar automatiskt filformatet.

```csharp
public PlainTextDocument(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen varifrån texten ska extraheras. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception/) | Dokumentet verkar vara skadat och kan inte läsas in. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklarna. |
| IOException | Det finns ett indata/utdata-undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du angav ett felaktigt lösenord. |
| ArgumentNullException | Strömmen kan inte vara null. |
| NotSupportedException | Strömmen stöder inte läsning eller sökning. |
| ObjectDisposedException | Strömmen är ett avfallsobjekt. |

## Anmärkningar

Dokumentet måste lagras i början av strömmen. Strömmen måste stödja slumpmässig positionering.

## Exempel

Visar hur man laddar innehållet i ett Microsoft Word-dokument i klartext med hjälp av stream.

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

* class [PlainTextDocument](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_1}

Skapar ett vanligt textdokument från en ström. Gör det möjligt att ange ytterligare alternativ, till exempel ett krypteringslösenord.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen varifrån texten ska extraheras. |
| loadOptions | LoadOptions | Ytterligare alternativ att använda när du laddar ett dokument. Kan vara`null`. |

### Undantag

| undantag | skick |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Dokumentformatet känns inte igen eller stöds inte. |
| [FileCorruptedException](../../filecorruptedexception/) | Dokumentet verkar vara skadat och kan inte läsas in. |
| Exception | Det finns ett problem med dokumentet och det bör rapporteras till Aspose.Words-utvecklarna. |
| IOException | Det finns ett indata/utdata-undantag. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Dokumentet är krypterat och kräver ett lösenord för att öppnas, men du angav ett felaktigt lösenord. |
| ArgumentNullException | Strömmen kan inte vara null. |
| NotSupportedException | Strömmen stöder inte läsning eller sökning. |
| ObjectDisposedException | Strömmen är ett avfallsobjekt. |

## Anmärkningar

Dokumentet måste lagras i början av strömmen. Strömmen måste stödja slumpmässig positionering.

## Exempel

Visar hur man laddar innehållet i ett krypterat Microsoft Word-dokument i klartext med hjälp av stream.

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

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
