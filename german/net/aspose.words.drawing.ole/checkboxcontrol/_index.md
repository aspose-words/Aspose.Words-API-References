---
title: CheckBoxControl Class
linktitle: CheckBoxControl
articleTitle: CheckBoxControl
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Ole.CheckBoxControl, um Kontrollkästchenwerte einfach umzuschalten und Ihre Dokumentautomatisierung durch nahtlose Integration zu verbessern.
type: docs
weight: 1440
url: /de/net/aspose.words.drawing.ole/checkboxcontrol/
---
## CheckBoxControl class

Das CheckBox-Steuerelement schaltet einen Wert um.

```csharp
public class CheckBoxControl : MorphDataControl
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Ruft die Hintergrundfarbe des Steuerelements ab oder legt sie fest. Der Standardwert hängt vom Typ des Steuerelements ab. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Ruft eine Caption-Eigenschaft des Steuerelements ab oder legt diese fest. Der Standardwert ist eine leere Zeichenfolge. |
| [Checked](../../aspose.words.drawing.ole/checkboxcontrol/checked/) { get; set; } | Ruft einen booleschen Wert ab oder setzt ihn, der entweder dies angibt`CheckBoxControl` aktiviert ist oder nicht. Der Standardwert ist`FALSCH` . |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Ruft eine Sammlung unmittelbar untergeordneter Steuerelemente ab. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Rückgaben`WAHR` wenn die Steuerung aktiviert ist. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Ruft eine Vordergrundfarbe des Steuerelements ab oder legt diese fest. Der Standardwert hängt vom Typ des Steuerelements ab. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Ruft eine Zeichenfolge ab oder legt sie fest, die eine Gruppe sich gegenseitig ausschließender Steuerelemente angibt. Der Standardwert ist eine leere Zeichenfolge. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Ruft die Höhe des Steuerelements in Punkten ab oder legt sie fest. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Rückgaben`WAHR` wenn das Steuerelement ein[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Ruft den Namen des ActiveX-Steuerelements ab oder legt ihn fest. |
| override [Type](../../aspose.words.drawing.ole/checkboxcontrol/type/) { get; } | Ruft den Typ des Forms 2.0-Steuerelements ab. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Ruft die zugrunde liegende Werteigenschaft ab, die häufig den Steuerelementstatus darstellt. Beispielsweise hat ein aktiviertes Optionsfeld den Wert „1“, während ein deaktiviertes den Wert „0“ hat. Der Standardwert ist eine leere Zeichenfolge. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Ruft die Breite des Steuerelements in Punkten ab oder legt sie fest. |

## Bemerkungen

Es gibt drei mögliche Zustände: ausgewählt, gelöscht und weder ausgewählt noch gelöscht, was eine Kombination aus Ein- und Aus-Zuständen bedeutet.

## Beispiele

Zeigt, wie der Status des CheckBox-Steuerelements geändert wird.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Siehe auch

* class [MorphDataControl](../morphdatacontrol/)
* namensraum [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../)
