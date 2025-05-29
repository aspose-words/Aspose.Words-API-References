---
title: Forms2OleControlType Enum
linktitle: Forms2OleControlType
articleTitle: Forms2OleControlType
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.Drawing.Ole.Forms2OleControlType, med en rad Forms 2.0-kontrolltyper för förbättrad dokumentautomation.
type: docs
weight: 1480
url: /sv/net/aspose.words.drawing.ole/forms2olecontroltype/
---
## Forms2OleControlType enumeration

Räknar upp typer av Forms 2.0-kontroller.

```csharp
public enum Forms2OleControlType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| OptionButton | `0` | En alternativknappskontroll. |
| Label | `1` | En kontroll som visar text. |
| Textbox | `2` | En kontroll som låter användaren ange text. |
| CheckBox | `3` | En kontroll som låter användaren markera eller avmarkera ett alternativ. |
| ToggleButton | `4` | En kontroll som låter användaren växla mellan två tillstånd. |
| SpinButton | `5` | En kontroll som låter användaren öka eller minska ett värde. |
| ComboBox | `6` | En kontroll som låter användaren välja ett objekt från en lista. |
| Frame | `7` | En kontroll som grupperar andra kontroller. |
| MultiPage | `8` | En kontroll som visar flera sidor med innehåll. |
| TabStrip | `9` | En kontroll som låter användaren växla mellan flera sidor med innehåll. |
| CommandButton | `10` | En knapp som utlöser en åtgärd när man klickar på den. |
| Image | `11` | En kontroll som visar en bild. |
| ScrollBar | `12` | En kontroll som låter användaren bläddra igenom innehåll. |
| Form | `13` | En behållare för andra kontroller. |
| ListBox | `14` | En kontroll som visar en lista med objekt. |

## Exempel

Visar hur man ändrar status för CheckBox-kontrollen.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Se även

* namnutrymme [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../)
