---
title: FileFormatUtil Class
linktitle: FileFormatUtil
articleTitle: FileFormatUtil
second_title: Aspose.Words per .NET
description: Gestisci i formati di file senza sforzo con Aspose.Words.FileFormatUtil. Rileva i formati e converti le estensioni senza problemi per una maggiore produttività.
type: docs
weight: 3230
url: /it/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Fornisce metodi di utilità per lavorare con i formati di file, come il rilevamento del formato di file o la conversione delle estensioni di file da/verso enumerazioni di formati di file.

Per saperne di più, visita il[Rileva il formato del file e controlla la compatibilità del formato](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) articolo di documentazione.

```csharp
public static class FileFormatUtil
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(*string*) | Converte il tipo di contenuto IANA in un valore enumerato del formato di caricamento. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(*string*) | Converte il tipo di contenuto IANA in un valore enumerato in formato di salvataggio. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(*Stream*) | Rileva e restituisce le informazioni sul formato di un documento memorizzato in un flusso. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(*string*) | Rileva e restituisce le informazioni sul formato di un documento memorizzato in un file su disco. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(*string*) | Converte un'estensione di nome file in un[`SaveFormat`](../saveformat/) valore. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(*[ImageType](../../aspose.words.drawing/imagetype/)*) | Converte un valore enumerato di tipo immagine Aspose.Words in un'estensione di file. L'estensione restituita è una stringa minuscola con un punto iniziale. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(*[LoadFormat](../loadformat/)*) | Converte un valore enumerato del formato di caricamento in un'estensione di file. L'estensione restituita è una stringa minuscola con un punto iniziale. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(*[LoadFormat](../loadformat/)*) | Converte un[`LoadFormat`](../loadformat/) valore a un[`SaveFormat`](../saveformat/) valore se possibile. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(*[SaveFormat](../saveformat/)*) | Converte un valore enumerato del formato di salvataggio in un'estensione di file. L'estensione restituita è una stringa minuscola con un punto iniziale. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(*[SaveFormat](../saveformat/)*) | Converte un[`SaveFormat`](../saveformat/) valore a un[`LoadFormat`](../loadformat/) valore se possibile. |

## Esempi

Mostra come rilevare la codifica in un file HTML.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// La proprietà Encoding viene utilizzata solo quando creiamo un oggetto FileFormatInfo per un documento HTML.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
