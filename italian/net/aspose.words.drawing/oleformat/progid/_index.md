---
title: OleFormat.ProgId
linktitle: ProgId
articleTitle: ProgId
second_title: Aspose.Words per .NET
description: Scopri la proprietà ProgId di OleFormat per gestire e personalizzare facilmente i ProgID degli oggetti OLE per ottenere funzionalità avanzate e un'integrazione perfetta.
type: docs
weight: 90
url: /it/net/aspose.words.drawing/oleformat/progid/
---
## OleFormat.ProgId property

Ottiene o imposta il ProgID dell'oggetto OLE.

```csharp
public string ProgId { get; set; }
```

## Osservazioni

La proprietà ProgID non è sempre presente nei documenti Microsoft Word e non è possibile farvi affidamento.

Non può essere`null`.

Il valore predefinito è una stringa vuota.

## Esempi

Mostra come estrarre oggetti OLE incorporati nei file.

```csharp
Document doc = new Document(MyDir + "OLE spreadsheet.docm");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

// L'oggetto OLE nella prima forma è un foglio di calcolo di Microsoft Excel.
OleFormat oleFormat = shape.OleFormat;

Assert.AreEqual("Excel.Sheet.12", oleFormat.ProgId);

// Il nostro oggetto non si aggiorna automaticamente né è bloccato dagli aggiornamenti.
Assert.False(oleFormat.AutoUpdate);
Assert.AreEqual(false, oleFormat.IsLocked);

// Se intendiamo salvare l'oggetto OLE in un file nel file system locale,
// possiamo usare la proprietà "SuggestedExtension" per determinare quale estensione file applicare al file.
Assert.AreEqual(".xlsx", oleFormat.SuggestedExtension);

// Di seguito sono riportati due metodi per salvare un oggetto OLE in un file nel file system locale.
// 1 - Salvalo tramite un flusso:
using (FileStream fs = new FileStream(ArtifactsDir + "OLE spreadsheet extracted via stream" + oleFormat.SuggestedExtension, FileMode.Create))
{
    oleFormat.Save(fs);
}

// 2 - Salvalo direttamente in un nome file:
oleFormat.Save(ArtifactsDir + "OLE spreadsheet saved directly" + oleFormat.SuggestedExtension);
```

### Guarda anche

* class [OleFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
