---
title: Forms2OleControl Class
linktitle: Forms2OleControl
articleTitle: Forms2OleControl
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Ole.Forms2OleControl, Ihre Lösung für die nahtlose Integration von Microsoft Forms 2.0 OLE-Steuerelementen in Ihre Anwendungen.
type: docs
weight: 1460
url: /de/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Stellt ein Microsoft Forms 2.0 OLE-Steuerelement dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit OLE-Objekten](https://docs.aspose.com/words/net/working-with-ole-objects/) Dokumentationsartikel.

```csharp
public abstract class Forms2OleControl : OleControl
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Ruft die Hintergrundfarbe des Steuerelements ab oder legt sie fest. Der Standardwert hängt vom Typ des Steuerelements ab. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Ruft eine Caption-Eigenschaft des Steuerelements ab oder legt diese fest. Der Standardwert ist eine leere Zeichenfolge. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Ruft eine Sammlung unmittelbar untergeordneter Steuerelemente ab. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Rückgaben`WAHR` wenn die Steuerung aktiviert ist. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Ruft eine Vordergrundfarbe des Steuerelements ab oder legt diese fest. Der Standardwert hängt vom Typ des Steuerelements ab. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Ruft eine Zeichenfolge ab oder legt sie fest, die eine Gruppe sich gegenseitig ausschließender Steuerelemente angibt. Der Standardwert ist eine leere Zeichenfolge. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Ruft die Höhe des Steuerelements in Punkten ab oder legt sie fest. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Rückgaben`WAHR` wenn das Steuerelement ein`Forms2OleControl` . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Ruft den Namen des ActiveX-Steuerelements ab oder legt ihn fest. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Ruft den Typ des Forms 2.0-Steuerelements ab. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Ruft die zugrunde liegende Werteigenschaft ab, die häufig den Steuerelementstatus darstellt. Beispielsweise hat ein aktiviertes Optionsfeld den Wert „1“, während ein deaktiviertes den Wert „0“ hat. Der Standardwert ist eine leere Zeichenfolge. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Ruft die Breite des Steuerelements in Punkten ab oder legt sie fest. |

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

* class [OleControl](../olecontrol/)
* namensraum [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../)
