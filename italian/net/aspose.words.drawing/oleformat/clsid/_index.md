---
title: OleFormat.Clsid
second_title: Aspose.Words per .NET API Reference
description: OleFormat proprietà. Ottiene il CLSID delloggetto OLE.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/oleformat/clsid/
---
## OleFormat.Clsid property

Ottiene il CLSID dell'oggetto OLE.

```csharp
public Guid Clsid { get; }
```

### Esempi

Mostra come accedere a un controllo OLE incorporato in un documento e ai relativi controlli figlio.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Le forme archiviano e visualizzano oggetti OLE nel corpo del documento.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Alcuni controlli OLE possono contenere controlli secondari, come quello in questo documento con tre pulsanti di opzione.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### Guarda anche

* class [OleFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../oleformat/)
* assemblea [Aspose.Words](../../../)


