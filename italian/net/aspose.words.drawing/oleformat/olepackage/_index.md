---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words per .NET
description: Accedi facilmente alle proprietà di OlePackage per gli oggetti OLE. Ottieni una perfetta integrazione con i pacchetti OLE e migliora le tue capacità di gestione dei dati.
type: docs
weight: 80
url: /it/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Fornire l'accesso a[`OlePackage`](../../olepackage/) se l'oggetto OLE è un pacchetto OLE. Restituisce`null` altrimenti.

```csharp
public OlePackage OlePackage { get; }
```

## Osservazioni

Il pacchetto OLE è una tecnologia legacy che consente di racchiudere qualsiasi formato di file non presente nel registro OLE di un sistema Windows in un pacchetto generico che consente di incorporare quasi tutto in un documento. Vedere[`OlePackage`](../../olepackage/) digita per maggiori informazioni.

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

* class [OlePackage](../../olepackage/)
* class [OleFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
