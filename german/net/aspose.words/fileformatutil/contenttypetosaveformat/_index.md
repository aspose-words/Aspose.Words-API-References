---
title: FileFormatUtil.ContentTypeToSaveFormat
linktitle: ContentTypeToSaveFormat
articleTitle: ContentTypeToSaveFormat
second_title: Aspose.Words für .NET
description: Konvertieren Sie IANA-Inhaltstypen mühelos in Speicherformatwerte mit der FileFormatUtil ContentTypeToSaveFormat-Methode. Optimieren Sie noch heute Ihre Dateiverwaltung!
type: docs
weight: 20
url: /de/net/aspose.words/fileformatutil/contenttypetosaveformat/
---
## FileFormatUtil.ContentTypeToSaveFormat method

Konvertiert den IANA-Inhaltstyp in einen aufgezählten Wert im sicheren Format.

```csharp
public static SaveFormat ContentTypeToSaveFormat(string contentType)
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentException | Wirft, wenn keine Konvertierung möglich ist. |

## Beispiele

Zeigt, wie Sie aus jeder Medientypzeichenfolge das entsprechende Aspose-Lade-/Speicherformat finden.

```csharp
    // Die Methoden ContentTypeToSaveFormat/ContentTypeToLoadFormat akzeptieren nur offizielle IANA-Medientypnamen, auch als MIME-Typen bekannt.
// Alle gültigen Medientypen sind hier aufgelistet: https://www.iana.org/assignments/media-types/media-types.xhtml.

// Der Versuch, ein SaveFormat mit einer teilweisen Medientypzeichenfolge zu verknüpfen, funktioniert nicht.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("jpeg"));

// Wenn Aspose.Words kein entsprechendes Speicher-/Ladeformat für einen Inhaltstyp hat, wird ebenfalls eine Ausnahme ausgelöst.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("application/zip"));

// Dateien der unten aufgeführten Typen können mit Aspose.Words gespeichert, aber nicht geladen werden.
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

// Bei Dateitypen, die gespeichert und geladen werden können, können wir einen Medientyp sowohl einem Ladeformat als auch einem Speicherformat zuordnen.
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

### Siehe auch

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
