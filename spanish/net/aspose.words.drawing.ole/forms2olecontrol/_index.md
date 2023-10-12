---
title: Class Forms2OleControl
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.Ole.Forms2OleControl clase. Representa el control OLE de Microsoft Forms 2.0.
type: docs
weight: 1110
url: /es/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Representa el control OLE de Microsoft Forms 2.0.

Para obtener más información, visite el[Trabajar con objetos antiguos](https://docs.aspose.com/words/net/working-with-ole-objects/) artículo de documentación.

```csharp
public abstract class Forms2OleControl : OleControl
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | Obtiene la propiedad Caption del control. El valor predeterminado es una cadena vacía. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Obtiene una colección de controles secundarios inmediatos. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Devoluciones`verdadero` si el control está en estado habilitado. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Obtiene o establece una cadena que especifica un grupo de controles mutuamente excluyentes. El valor predeterminado es una cadena vacía. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Devoluciones`verdadero` si el control es un`Forms2OleControl` . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Obtiene o establece el nombre del control ActiveX. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Obtiene el tipo de control de Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Obtiene la propiedad Valor subyacente que a menudo representa el estado de control. Por ejemplo, el botón de opción marcado tiene el valor '1', mientras que el que no está marcado tiene '0'. El valor predeterminado es una cadena vacía. |

### Ejemplos

Muestra cómo verificar las propiedades de un control ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Tenga en cuenta que no puede configurar GroupName para un marco.
    checkBox.GroupName = "Aspose group name";
}
```

### Ver también

* class [OleControl](../olecontrol/)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../)


