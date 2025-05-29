---
title: OlePackage.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words per .NET
description: Scopri la proprietà OlePackage FileName per gestire facilmente i nomi dei file dei pacchetti OLE. Migliora la gestione dei dati con un'integrazione perfetta e flessibilità.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/olepackage/filename/
---
## OlePackage.FileName property

Ottiene o imposta il nome del file del pacchetto OLE.

```csharp
public string FileName { get; set; }
```

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

* class [OlePackage](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
