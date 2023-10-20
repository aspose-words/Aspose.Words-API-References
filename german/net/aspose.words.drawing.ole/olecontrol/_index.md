---
title: OleControl Class
linktitle: OleControl
articleTitle: OleControl
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.Ole.OleControl klas. Stellt das OLE ActiveXSteuerelement dar in C#.
type: docs
weight: 1140
url: /de/net/aspose.words.drawing.ole/olecontrol/
---
## OleControl class

Stellt das OLE ActiveX-Steuerelement dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Ole-Objekten](https://docs.aspose.com/words/net/working-with-ole-objects/) Dokumentationsartikel.

```csharp
public class OleControl
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Gibt zurück`WAHR` wenn die Kontrolle a ist[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Ruft den Namen des ActiveX-Steuerelements ab oder legt diesen fest. |

## Beispiele

Zeigt, wie die Eigenschaften eines ActiveX-Steuerelements überprüft werden.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Beachten Sie, dass Sie GroupName nicht für einen Frame festlegen können.
    checkBox.GroupName = "Aspose group name";
}
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../)
