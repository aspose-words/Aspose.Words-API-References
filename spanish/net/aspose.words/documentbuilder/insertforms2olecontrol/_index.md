---
title: DocumentBuilder.InsertForms2OleControl
linktitle: InsertForms2OleControl
articleTitle: InsertForms2OleControl
second_title: Aspose.Words para .NET
description: Integre fácilmente Forms2OleControl con el método InsertForms2OleControl de DocumentBuilder. ¡Mejore la funcionalidad de sus documentos hoy mismo!
type: docs
weight: 350
url: /es/net/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder.InsertForms2OleControl method

Inserciones[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/) objeto en la posición actual.

```csharp
public Shape InsertForms2OleControl(Forms2OleControl forms2OleControl)
```

### Valor_devuelto

[`Shape`](../../../aspose.words.drawing/shape/) objeto que contiene lo pasado[`Forms2OleControl`](../../../aspose.words.drawing.ole/forms2olecontrol/)

## Ejemplos

Muestra cómo insertar un control ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Ver también

* property [OleFormat](../../../aspose.words.drawing/shape/oleformat/)
* property [OleControl](../../../aspose.words.drawing/oleformat/olecontrol/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [Forms2OleControl](../../../aspose.words.drawing.ole/forms2olecontrol/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
