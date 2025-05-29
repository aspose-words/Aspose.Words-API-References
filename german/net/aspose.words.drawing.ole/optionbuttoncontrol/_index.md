---
title: OptionButtonControl Class
linktitle: OptionButtonControl
articleTitle: OptionButtonControl
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Ole.OptionButtonControl, die sich perfekt für die Erstellung exklusiver Auswahlmöglichkeiten in Ihren Anwendungen eignet. Verbessern Sie noch heute das Benutzererlebnis!
type: docs
weight: 1510
url: /de/net/aspose.words.drawing.ole/optionbuttoncontrol/
---
## OptionButtonControl class

Das OptionButton-Steuerelement ermöglicht eine einzelne Auswahl aus einer begrenzten Menge sich gegenseitig ausschließender Auswahlmöglichkeiten.

```csharp
public class OptionButtonControl : MorphDataControl
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
| [Selected](../../aspose.words.drawing.ole/optionbuttoncontrol/selected/) { get; set; } | Ruft einen booleschen Wert ab oder setzt ihn, der entweder dies angibt`OptionButtonControl` ausgewählt ist oder nicht. |
| override [Type](../../aspose.words.drawing.ole/optionbuttoncontrol/type/) { get; } | Ruft den Typ des Forms 2.0-Steuerelements ab. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Ruft die zugrunde liegende Werteigenschaft ab, die häufig den Steuerelementstatus darstellt. Beispielsweise hat ein aktiviertes Optionsfeld den Wert „1“, während ein deaktiviertes den Wert „0“ hat. Der Standardwert ist eine leere Zeichenfolge. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Ruft die Breite des Steuerelements in Punkten ab oder legt sie fest. |

## Beispiele

Zeigt, wie ein Optionsfeld ausgewählt wird.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Auswahl des ersten ausgewählten Elements aufheben.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// Wählen Sie die zweite Optionsschaltfläche aus.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### Siehe auch

* class [MorphDataControl](../morphdatacontrol/)
* namensraum [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../)
