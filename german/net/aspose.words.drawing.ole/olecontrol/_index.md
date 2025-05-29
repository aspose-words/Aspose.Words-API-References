---
title: OleControl Class
linktitle: OleControl
articleTitle: OleControl
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Ole.OleControl, um OLE-ActiveX-Steuerelemente nahtlos in Ihre Anwendungen zu integrieren und so die Funktionalität zu verbessern.
type: docs
weight: 1500
url: /de/net/aspose.words.drawing.ole/olecontrol/
---
## OleControl class

Stellt ein OLE ActiveX-Steuerelement dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit OLE-Objekten](https://docs.aspose.com/words/net/working-with-ole-objects/) Dokumentationsartikel.

```csharp
public class OleControl
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Rückgaben`WAHR` wenn das Steuerelement ein[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Ruft den Namen des ActiveX-Steuerelements ab oder legt ihn fest. |

## Beispiele

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.AreEqual("First", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Beachten Sie, dass Sie für einen Frame keinen Gruppennamen festlegen können.
    checkBox.GroupName = "Aspose group name";
}
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../)
