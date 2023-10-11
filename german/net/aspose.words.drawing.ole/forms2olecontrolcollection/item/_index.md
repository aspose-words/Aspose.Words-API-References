---
title: Forms2OleControlCollection.Item
second_title: Aspose.Words für .NET-API-Referenz
description: Forms2OleControlCollection eigendom. Ruft abForms2OleControl Objekt an einem angegebenen Index.
type: docs
weight: 30
url: /de/net/aspose.words.drawing.ole/forms2olecontrolcollection/item/
---
## Forms2OleControlCollection indexer

Ruft ab[`Forms2OleControl`](../../forms2olecontrol/) Objekt an einem angegebenen Index.

```csharp
public Forms2OleControl this[int index] { get; }
```

### Beispiele

Zeigt, wie auf ein in ein Dokument eingebettetes OLE-Steuerelement und seine untergeordneten Steuerelemente zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Formen speichern und zeigen OLE-Objekte im Hauptteil des Dokuments an.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Einige OLE-Steuerelemente enthalten möglicherweise untergeordnete Steuerelemente, z. B. das in diesem Dokument mit drei Optionsschaltflächen.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### Siehe auch

* class [Forms2OleControl](../../forms2olecontrol/)
* class [Forms2OleControlCollection](../)
* namensraum [Aspose.Words.Drawing.Ole](../../forms2olecontrolcollection/)
* Montage [Aspose.Words](../../../)


