---
title: CommandButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „CommandButtonControl Type“, um einfach auf Forms 2.0-Steuerelementtypen zuzugreifen und so die Funktionalität und Benutzererfahrung Ihrer Anwendung zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.ole/commandbuttoncontrol/type/
---
## CommandButtonControl.Type property

Ruft den Typ des Forms 2.0-Steuerelements ab.

```csharp
public override Forms2OleControlType Type { get; }
```

## Beispiele

Zeigt, wie ein ActiveX-Steuerelement eingefügt wird.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Siehe auch

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CommandButtonControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
