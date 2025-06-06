---
title: OleFormat.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words per .NET
description: Scopri il metodo OleFormat Save per archiviare in modo efficiente i dati degli oggetti incorporati nel flusso che preferisci. Migliora la gestione dei dati con facilità!
type: docs
weight: 160
url: /it/net/aspose.words.drawing/oleformat/save/
---
## Save(*Stream*) {#save}

Salva i dati dell'oggetto incorporato nel flusso specificato.

```csharp
public void Save(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Dove salvare i dati dell'oggetto. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidOperationException | Viene generato se si tenta di salvare un oggetto collegato. |

## Osservazioni

È responsabilità del chiamante smaltire il flusso.

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

---

## Save(*string*) {#save_1}

Salva i dati dell'oggetto incorporato in un file con il nome specificato.

```csharp
public void Save(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Nome del file in cui salvare i dati dell'oggetto OLE. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidOperationException | Viene generato se si tenta di salvare un oggetto collegato. |

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
