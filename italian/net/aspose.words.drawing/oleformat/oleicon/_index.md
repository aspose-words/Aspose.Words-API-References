---
title: OleFormat.OleIcon
linktitle: OleIcon
articleTitle: OleIcon
second_title: Aspose.Words per .NET
description: OleFormat OleIcon proprietà. Ottiene laspetto di disegno delloggetto OLE. QuandoVERO  loggetto OLE viene visualizzato come icona. Quandofalso  loggetto OLE viene visualizzato come content in C#.
type: docs
weight: 70
url: /it/net/aspose.words.drawing/oleformat/oleicon/
---
## OleFormat.OleIcon property

Ottiene l'aspetto di disegno dell'oggetto OLE. Quando`VERO` , l'oggetto OLE viene visualizzato come icona. Quando`falso` , l'oggetto OLE viene visualizzato come content.

```csharp
public bool OleIcon { get; }
```

## Osservazioni

Aspose.Words non consente di impostare questa proprietà per evitare confusione. Se fossi in grado di cambiare l'aspetto di disegno in Aspose.Words, Microsoft Word visualizzerebbe comunque l'oggetto OLE nel suo aspetto di disegno originale finché non modifichi o aggiorni l'oggetto OLE in Microsoft Word.

## Esempi

Mostra come inserire oggetti OLE collegati e scollegati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Incorpora un disegno di Microsoft Visio nel documento come oggetto OLE.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", false, false, null);

// Inserisci un collegamento al file nel file system locale e visualizzalo come un'icona.
builder.InsertOleObject(ImageDir + "Microsoft Visio drawing.vsd", "Package", true, true, null);

// L'inserimento di oggetti OLE crea forme che memorizzano questi oggetti.
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

// Se l'oggetto contiene dati OLE, possiamo accedervi utilizzando uno stream.
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
