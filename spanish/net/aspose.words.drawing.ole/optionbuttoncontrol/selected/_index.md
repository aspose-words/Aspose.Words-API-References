---
title: OptionButtonControl.Selected
linktitle: Selected
articleTitle: Selected
second_title: Aspose.Words para .NET
description: ¡Administra tu OptionButtonControl fácilmente! Establece u obtén su estado seleccionado con un simple valor booleano para una interacción fluida con el usuario.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.ole/optionbuttoncontrol/selected/
---
## OptionButtonControl.Selected property

Obtiene o establece un valor booleano que indica esto[`OptionButtonControl`](../) está seleccionado o no.

```csharp
public bool Selected { get; set; }
```

## Observaciones

Nota: esta propiedad le permite seleccionar varios elementos en un grupo de[`OptionButtonControl`](../) con el mismo[`GroupName`](../../forms2olecontrol/groupname/) Depende de usted encargarse de deseleccionar un elemento seleccionado previamente cuando realiza esta[`OptionButtonControl`](../) seleccionado.

## Ejemplos

Muestra cómo seleccionar el botón de opción.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Deseleccionar el primer elemento seleccionado.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// Seleccione el segundo botón de opción.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### Ver también

* class [OptionButtonControl](../)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../../)
