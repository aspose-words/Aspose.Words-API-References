---
title: CommandButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Scopri la proprietà CommandButtonControl Type per accedere facilmente ai tipi di controllo di Forms 2.0, migliorando la funzionalità e l'esperienza utente della tua applicazione.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.ole/commandbuttoncontrol/type/
---
## CommandButtonControl.Type property

Ottiene il tipo di controllo Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CommandButtonControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
