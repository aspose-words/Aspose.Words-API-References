---
title: Forms2OleControlType Enum
linktitle: Forms2OleControlType
articleTitle: Forms2OleControlType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.Ole.Forms2OleControlType mit einer Reihe von Forms 2.0-Steuerelementtypen für eine verbesserte Dokumentautomatisierung.
type: docs
weight: 1480
url: /de/net/aspose.words.drawing.ole/forms2olecontroltype/
---
## Forms2OleControlType enumeration

Listet die Typen von Forms 2.0-Steuerelementen auf.

```csharp
public enum Forms2OleControlType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| OptionButton | `0` | Ein Optionsfeld-Steuerelement. |
| Label | `1` | Ein Steuerelement, das Text anzeigt. |
| Textbox | `2` | Ein Steuerelement, das dem Benutzer die Eingabe von Text ermöglicht. |
| CheckBox | `3` | Ein Steuerelement, mit dem der Benutzer eine Option auswählen oder abwählen kann. |
| ToggleButton | `4` | Ein Steuerelement, das dem Benutzer das Umschalten zwischen zwei Zuständen ermöglicht. |
| SpinButton | `5` | Ein Steuerelement, mit dem der Benutzer einen Wert erhöhen oder verringern kann. |
| ComboBox | `6` | Ein Steuerelement, mit dem der Benutzer ein Element aus einer Liste auswählen kann. |
| Frame | `7` | Ein Steuerelement, das andere Steuerelemente gruppiert. |
| MultiPage | `8` | Ein Steuerelement, das mehrere Inhaltsseiten anzeigt. |
| TabStrip | `9` | Ein Steuerelement, das dem Benutzer das Wechseln zwischen mehreren Inhaltsseiten ermöglicht. |
| CommandButton | `10` | Eine Schaltfläche, die beim Klicken eine Aktion auslöst. |
| Image | `11` | Ein Steuerelement, das ein Bild anzeigt. |
| ScrollBar | `12` | Ein Steuerelement, mit dem der Benutzer durch Inhalte blättern kann. |
| Form | `13` | Ein Container für andere Steuerelemente. |
| ListBox | `14` | Ein Steuerelement, das eine Liste von Elementen anzeigt. |

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

* namensraum [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../)
