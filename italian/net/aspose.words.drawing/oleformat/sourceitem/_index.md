---
title: OleFormat.SourceItem
linktitle: SourceItem
articleTitle: SourceItem
second_title: Aspose.Words per .NET
description: Scopri la proprietà SourceItem di OleFormat, identifica e gestisci facilmente le parti collegate del tuo file sorgente con questa funzionalità essenziale delle stringhe.
type: docs
weight: 110
url: /it/net/aspose.words.drawing/oleformat/sourceitem/
---
## OleFormat.SourceItem property

Ottiene o imposta una stringa utilizzata per identificare la parte del file sorgente che viene collegata.

```csharp
public string SourceItem { get; set; }
```

## Osservazioni

Il valore predefinito è una stringa vuota.

Ad esempio, se il file di origine è una cartella di lavoro di Microsoft Excel,`SourceItem` La proprietà potrebbe restituire "Workbook1!R3C1:R4C2" se l'oggetto OLE contiene solo alcune celle del foglio di lavoro.

## Esempi

Mostra come inserire oggetti OLE collegati e non collegati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Incorpora un disegno di Microsoft Visio nel documento come oggetto OLE.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Inserisce un collegamento al file nel file system locale e lo visualizza come icona.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// L'inserimento di oggetti OLE crea forme che memorizzano tali oggetti.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);
Assert.AreEqual(2, shapes.Count(s => s.ShapeType == ShapeType.OleObject));

// Se una forma contiene un oggetto OLE, avrà una proprietà "OleFormat" valida,
// che possiamo utilizzare per verificare alcuni aspetti della forma.
OleFormat oleFormat = shapes[0].OleFormat;

Assert.AreEqual(false, oleFormat.IsLink);
Assert.AreEqual(false, oleFormat.OleIcon);

oleFormat = shapes[1].OleFormat;

Assert.AreEqual(true, oleFormat.IsLink);
Assert.AreEqual(true, oleFormat.OleIcon);

Assert.True(oleFormat.SourceFullName.EndsWith(@"Images" + Path.DirectorySeparatorChar + "Microsoft Visio drawing.vsd"));
Assert.AreEqual("", oleFormat.SourceItem);

Assert.AreEqual("Microsoft Visio drawing.vsd", oleFormat.IconCaption);

doc.Save(ArtifactsDir + "Shape.OleLinks.docx");

// Se l'oggetto contiene dati OLE, possiamo accedervi tramite un flusso.
using (MemoryStream stream = oleFormat.GetOleEntry("\x0001CompObj"))
{
    byte[] oleEntryBytes = stream.ToArray();
    Assert.AreEqual(76, oleEntryBytes.Length);
}
```

### Guarda anche

* class [OleFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
