---
title: CommandButtonControl
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words per .NET
description: Scopri il costruttore CommandButtonControl. Crea e personalizza facilmente i pulsanti per le tue applicazioni con questa potente istanza di classe.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.ole/commandbuttoncontrol/commandbuttoncontrol/
---
## CommandButtonControl constructor

Inizializza una nuova istanza di[`CommandButtonControl`](../) classe.

```csharp
public CommandButtonControl()
```

## Esempi

Mostra come inserire un controllo ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Guarda anche

* class [CommandButtonControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
