---
title: CommandButtonControl Class
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Ole.CommandButtonControl, um ganz einfach interaktive Schaltflächen zu erstellen, die Makros ausführen und so die Benutzerinteraktion mit Ihren Anwendungen verbessern.
type: docs
weight: 1450
url: /de/net/aspose.words.drawing.ole/commandbuttoncontrol/
---
## CommandButtonControl class

Das CommandButton-Steuerelement führt ein Makro aus, das eine Aktion ausführt, wenn ein Benutzer darauf klickt.

```csharp
public class CommandButtonControl : Forms2OleControl
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CommandButtonControl](commandbuttoncontrol/)() | Initialisiert eine neue Instanz von`CommandButtonControl` Klasse. |

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
| override [Type](../../aspose.words.drawing.ole/commandbuttoncontrol/type/) { get; } | Ruft den Typ des Forms 2.0-Steuerelements ab. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Ruft die zugrunde liegende Werteigenschaft ab, die häufig den Steuerelementstatus darstellt. Beispielsweise hat ein aktiviertes Optionsfeld den Wert „1“, während ein deaktiviertes den Wert „0“ hat. Der Standardwert ist eine leere Zeichenfolge. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Ruft die Breite des Steuerelements in Punkten ab oder legt sie fest. |

## Beispiele

Zeigt, wie ein ActiveX-Steuerelement eingefügt wird.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Siehe auch

* class [Forms2OleControl](../forms2olecontrol/)
* namensraum [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../)
