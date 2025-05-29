---
title: OleFormat.IconCaption
linktitle: IconCaption
articleTitle: IconCaption
second_title: Aspose.Words per .NET
description: Scopri la proprietà OleFormat IconCaption per recuperare e personalizzare facilmente le didascalie delle icone degli oggetti OLE per una presentazione migliore dei documenti.
type: docs
weight: 30
url: /it/net/aspose.words.drawing/oleformat/iconcaption/
---
## OleFormat.IconCaption property

Ottiene la didascalia dell'icona dell'oggetto OLE.

Nel caso in cui l'oggetto OLE non abbia un'icona o non sia possibile recuperare una didascalia, restituisce una stringa empty .

```csharp
public string IconCaption { get; }
```

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
