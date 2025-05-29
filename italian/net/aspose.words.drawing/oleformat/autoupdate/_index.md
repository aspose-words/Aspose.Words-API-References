---
title: OleFormat.AutoUpdate
linktitle: AutoUpdate
articleTitle: AutoUpdate
second_title: Aspose.Words per .NET
description: Scopri la proprietà OleFormat AutoUpdate in Microsoft Word, che garantisce che i collegamenti agli oggetti OLE restino aggiornati e migliorano la precisione dei documenti senza sforzo.
type: docs
weight: 10
url: /it/net/aspose.words.drawing/oleformat/autoupdate/
---
## OleFormat.AutoUpdate property

Specifica se il collegamento all'oggetto OLE viene aggiornato automaticamente o meno in Microsoft Word.

```csharp
public bool AutoUpdate { get; set; }
```

## Osservazioni

Il valore predefinito è`falso`.

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
