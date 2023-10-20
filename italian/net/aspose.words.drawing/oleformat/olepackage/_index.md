---
title: OleFormat.OlePackage
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words per .NET
description: OleFormat OlePackage proprietà. Fornisci laccesso aOlePackage se loggetto OLE è un pacchetto OLE. Restituiscenullo altrimenti in C#.
type: docs
weight: 80
url: /it/net/aspose.words.drawing/oleformat/olepackage/
---
## OleFormat.OlePackage property

Fornisci l'accesso a[`OlePackage`](../../olepackage/) se l'oggetto OLE è un pacchetto OLE. Restituisce`nullo` altrimenti.

```csharp
public OlePackage OlePackage { get; }
```

## Osservazioni

Il pacchetto OLE è una tecnologia legacy che consente di racchiudere qualsiasi formato di file non presente nel registro OLE di un sistema Windows in un pacchetto generico che consente di incorporare quasi qualsiasi cosa in un documento. Vedi[`OlePackage`](../../olepackage/) digita per maggiori informazioni.

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
