---
title: CommandButtonControl
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words für .NET
description: Entdecken Sie den CommandButtonControl-Konstruktor. Mit dieser leistungsstarken Klasseninstanz erstellen und passen Sie mühelos Schaltflächen für Ihre Anwendungen an.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.ole/commandbuttoncontrol/commandbuttoncontrol/
---
## CommandButtonControl constructor

Initialisiert eine neue Instanz von[`CommandButtonControl`](../) Klasse.

```csharp
public CommandButtonControl()
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

* class [CommandButtonControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
