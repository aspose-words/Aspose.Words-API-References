---
title: FileFormatUtil.ContentTypeToLoadFormat
linktitle: ContentTypeToLoadFormat
articleTitle: ContentTypeToLoadFormat
second_title: Aspose.Words per .NET
description: Trasforma senza sforzo i tipi di contenuto IANA in valori di formato di caricamento con il metodo FileFormatUtil ContentTypeToLoadFormat. Semplifica la gestione dei tuoi file oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words/fileformatutil/contenttypetoloadformat/
---
## FileFormatUtil.ContentTypeToLoadFormat method

Converte il tipo di contenuto IANA in un valore enumerato del formato di caricamento.

```csharp
public static LoadFormat ContentTypeToLoadFormat(string contentType)
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentException | Genera un errore quando non è possibile convertire. |

## Esempi

Mostra come trovare il formato di caricamento/salvataggio Aspose corrispondente da ogni stringa di tipo di supporto.

```csharp
 // I metodi ContentTypeToSaveFormat/ContentTypeToLoadFormat accettano solo nomi di tipi di supporto IANA ufficiali, noti anche come tipi MIME.
// Tutti i tipi di media validi sono elencati qui: https://www.iana.org/assignments/media-types/media-types.xhtml.

// Il tentativo di associare un SaveFormat a una stringa di tipo di supporto parziale non funzionerà.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("jpeg"));

// Se Aspose.Words non ha un formato di salvataggio/caricamento corrispondente per un tipo di contenuto, verrà generata anche un'eccezione.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("application/zip"));

// I file dei tipi elencati di seguito possono essere salvati, ma non caricati tramite Aspose.Words.
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

// Per i tipi di file che possono essere salvati e caricati, possiamo abbinare un tipo di supporto sia a un formato di caricamento che a un formato di salvataggio.
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

### Guarda anche

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
