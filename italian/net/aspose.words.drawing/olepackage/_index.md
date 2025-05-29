---
title: OlePackage Class
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.Drawing.OlePackage per gestire facilmente le proprietà del pacchetto OLE e migliorare le capacità di elaborazione dei documenti.
type: docs
weight: 1540
url: /it/net/aspose.words.drawing/olepackage/
---
## OlePackage class

Consente di accedere alle proprietà del pacchetto OLE.

Per saperne di più, visita il[Lavorare con oggetti Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) articolo di documentazione.

```csharp
public class OlePackage
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | Ottiene o imposta il nome visualizzato del pacchetto OLE. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | Ottiene o imposta il nome del file del pacchetto OLE. |

## Osservazioni

Il pacchetto OLE è un metodo obsoleto e "non documentato" per archiviare oggetti incorporati se il gestore OLE è sconosciuto. Le prime versioni di Windows, come Windows 3.1, 95 e 98, avevano l'applicazione Packager.exe che poteva essere utilizzata per incorporare qualsiasi tipo di dati in un documento. Ora questa applicazione è esclusa da Windows, ma MS Word e altre applicazioni la usano ancora per incorporare dati se il gestore OLE è mancante o sconosciuto.

## Esempi

Mostra come inserire un oggetto OLE in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Gli oggetti OLE ci consentono di aprire altri file nel file system locale utilizzando un'altra applicazione installata
// nel nostro sistema operativo facendo doppio clic sulla forma che contiene l'oggetto OLE nel corpo del documento.
// In questo caso, il nostro file esterno sarà un archivio ZIP.
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
