---
title: DocumentBuilder.InsertForms2OleControl
linktitle: InsertForms2OleControl
articleTitle: InsertForms2OleControl
second_title: Aspose.Words für .NET
description: Integrieren Sie Forms2OleControl mühelos mit der InsertForms2OleControl-Methode von DocumentBuilder. Erweitern Sie noch heute die Funktionalität Ihrer Dokumente!
type: docs
weight: 350
url: /de/net/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder.InsertForms2OleControl method

Einsätze[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/) Objekt in aktuelle Position.

```csharp
public Shape InsertForms2OleControl(Forms2OleControl forms2OleControl)
```

### Rückgabewert

[`Shape`](../../../aspose.words.drawing/shape/) Objekt, das übergeben enthält[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/)

## Beispiele

Zeigt, wie ein ActiveX-Steuerelement eingefügt wird.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Siehe auch

* property [OleFormat](../../../aspose.words.drawing/shape/oleformat/)
* property [OleControl](../../../aspose.words.drawing/oleformat/olecontrol/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
