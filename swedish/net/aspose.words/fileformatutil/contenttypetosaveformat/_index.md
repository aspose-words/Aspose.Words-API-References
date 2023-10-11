---
title: FileFormatUtil.ContentTypeToSaveFormat
second_title: Aspose.Words för .NET API Referens
description: FileFormatUtil metod. Konverterar IANAinnehållstyp till ett sparat format uppräknat värde.
type: docs
weight: 20
url: /sv/net/aspose.words/fileformatutil/contenttypetosaveformat/
---
## FileFormatUtil.ContentTypeToSaveFormat method

Konverterar IANA-innehållstyp till ett sparat format uppräknat värde.

```csharp
public static SaveFormat ContentTypeToSaveFormat(string contentType)
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentException | Kastar när det inte går att konvertera. |

### Exempel

Visar hur man hittar motsvarande Aspose-laddnings-/sparaformat från varje mediatypsträng.

```csharp
 // ContentTypeToSaveFormat/ContentTypeToLoadFormat-metoderna accepterar endast officiella IANA-mediatypnamn, även kända som MIME-typer.
// Alla giltiga mediatyper listas här: https://www.iana.org/assignments/media-types/media-types.xhtml.

// Att försöka associera ett SaveFormat med en partiell mediatypsträng kommer inte att fungera.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("jpeg"));

// Om Aspose.Words inte har ett motsvarande spara/ladda format för en innehållstyp, kommer ett undantag också att kastas.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("application/zip"));

// Filer av de typer som anges nedan kan sparas, men inte laddas med Aspose.Words.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToLoadFormat("image/jpeg"));

Assert.AreEqual(SaveFormat.Jpeg, FileFormatUtil.ContentTypeToSaveFormat("image/jpeg"));
Assert.AreEqual(SaveFormat.Png, FileFormatUtil.ContentTypeToSaveFormat("image/png"));
Assert.AreEqual(SaveFormat.Tiff, FileFormatUtil.ContentTypeToSaveFormat("image/tiff"));
Assert.AreEqual(SaveFormat.Gif, FileFormatUtil.ContentTypeToSaveFormat("image/gif"));
Assert.AreEqual(SaveFormat.Emf, FileFormatUtil.ContentTypeToSaveFormat("image/x-emf"));
Assert.AreEqual(SaveFormat.Xps, FileFormatUtil.ContentTypeToSaveFormat("application/vnd.ms-xpsdocument"));
Assert.AreEqual(SaveFormat.Pdf, FileFormatUtil.ContentTypeToSaveFormat("application/pdf"));
Assert.AreEqual(SaveFormat.Svg, FileFormatUtil.ContentTypeToSaveFormat("image/svg+xml"));
Assert.AreEqual(SaveFormat.Epub, FileFormatUtil.ContentTypeToSaveFormat("application/epub+zip"));

// För filtyper som kan sparas och laddas kan vi matcha en mediatyp med både ett laddningsformat och ett sparaformat.
Assert.AreEqual(LoadFormat.Doc, FileFormatUtil.ContentTypeToLoadFormat("application/msword"));
Assert.AreEqual(SaveFormat.Doc, FileFormatUtil.ContentTypeToSaveFormat("application/msword"));

Assert.AreEqual(LoadFormat.Docx,
    FileFormatUtil.ContentTypeToLoadFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));
Assert.AreEqual(SaveFormat.Docx,
    FileFormatUtil.ContentTypeToSaveFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));

Assert.AreEqual(LoadFormat.Text, FileFormatUtil.ContentTypeToLoadFormat("text/plain"));
Assert.AreEqual(SaveFormat.Text, FileFormatUtil.ContentTypeToSaveFormat("text/plain"));

Assert.AreEqual(LoadFormat.Rtf, FileFormatUtil.ContentTypeToLoadFormat("application/rtf"));
Assert.AreEqual(SaveFormat.Rtf, FileFormatUtil.ContentTypeToSaveFormat("application/rtf"));

Assert.AreEqual(LoadFormat.Html, FileFormatUtil.ContentTypeToLoadFormat("text/html"));
Assert.AreEqual(SaveFormat.Html, FileFormatUtil.ContentTypeToSaveFormat("text/html"));

Assert.AreEqual(LoadFormat.Mhtml, FileFormatUtil.ContentTypeToLoadFormat("multipart/related"));
Assert.AreEqual(SaveFormat.Mhtml, FileFormatUtil.ContentTypeToSaveFormat("multipart/related"));
```

### Se även

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* namnutrymme [Aspose.Words](../../fileformatutil/)
* hopsättning [Aspose.Words](../../../)


