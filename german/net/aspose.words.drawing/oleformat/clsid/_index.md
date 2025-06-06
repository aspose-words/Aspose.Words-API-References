---
title: OleFormat.Clsid
linktitle: Clsid
articleTitle: Clsid
second_title: Aspose.Words für .NET
description: Entdecken Sie die OleFormat Clsid-Eigenschaft, um die CLSID von OLE-Objekten einfach abzurufen und so die Funktionalität und Leistung Ihrer Anwendung zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/oleformat/clsid/
---
## OleFormat.Clsid property

Ruft die CLSID des OLE-Objekts ab.

```csharp
public Guid Clsid { get; }
```

## Beispiele

Zeigt, wie auf ein in ein Dokument eingebettetes OLE-Steuerelement und seine untergeordneten Steuerelemente zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Formen speichern und zeigen OLE-Objekte im Hauptteil des Dokuments an.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Einige OLE-Steuerelemente können untergeordnete Steuerelemente enthalten, wie beispielsweise das in diesem Dokument mit drei Optionsschaltflächen.
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

* class [OleFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
