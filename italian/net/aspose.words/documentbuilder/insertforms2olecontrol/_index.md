---
title: DocumentBuilder.InsertForms2OleControl
linktitle: InsertForms2OleControl
articleTitle: InsertForms2OleControl
second_title: Aspose.Words per .NET
description: Integra senza sforzo Forms2OleControl con il metodo InsertForms2OleControl di DocumentBuilder. Migliora le funzionalità dei tuoi documenti oggi stesso!
type: docs
weight: 350
url: /it/net/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder.InsertForms2OleControl method

Inserimenti[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/) oggetto nella posizione corrente.

```csharp
public Shape InsertForms2OleControl(Forms2OleControl forms2OleControl)
```

### Valore di ritorno

[`Shape`](../../../aspose.words.drawing/shape/) oggetto che contiene passato[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/)

## Esempi

Mostra come inserire un controllo ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Guarda anche

* property [OleFormat](../../../aspose.words.drawing/shape/oleformat/)
* property [OleControl](../../../aspose.words.drawing/oleformat/olecontrol/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
