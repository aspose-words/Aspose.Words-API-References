---
title: TextBoxControl Class
linktitle: TextBoxControl
articleTitle: TextBoxControl
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Ole.TextBoxControl, um mühelos organisierten Text aus Daten oder Benutzereingaben anzuzeigen. Optimieren Sie noch heute Ihr Dokumentenmanagement!
type: docs
weight: 1520
url: /de/net/aspose.words.drawing.ole/textboxcontrol/
---
## TextBoxControl class

Das TextBox-Steuerelement zeigt Text aus einem organisierten Datensatz oder einer Benutzereingabe an.

```csharp
public class TextBoxControl : MorphDataControl
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
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Rückgaben`WAHR` wenn das Steuerelement ein[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Ruft den Namen des ActiveX-Steuerelements ab oder legt ihn fest. |
| [Text](../../aspose.words.drawing.ole/textboxcontrol/text/) { get; set; } | Ruft einen Text des Steuerelements ab oder legt ihn fest. |
| override [Type](../../aspose.words.drawing.ole/textboxcontrol/type/) { get; } | Ruft den Typ des Forms 2.0-Steuerelements ab. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Ruft die zugrunde liegende Werteigenschaft ab, die häufig den Steuerelementstatus darstellt. Beispielsweise hat ein aktiviertes Optionsfeld den Wert „1“, während ein deaktiviertes den Wert „0“ hat. Der Standardwert ist eine leere Zeichenfolge. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Ruft die Breite des Steuerelements in Punkten ab oder legt sie fest. |

## Beispiele

Zeigt, wie der Text des TextBox-OLE-Steuerelements geändert wird.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Siehe auch

* class [MorphDataControl](../morphdatacontrol/)
* namensraum [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../)
