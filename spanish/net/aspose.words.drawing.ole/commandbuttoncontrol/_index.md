---
title: CommandButtonControl Class
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Ole.CommandButtonControl para crear fácilmente botones interactivos que ejecutan macros, mejorando la participación del usuario en sus aplicaciones.
type: docs
weight: 1450
url: /es/net/aspose.words.drawing.ole/commandbuttoncontrol/
---
## CommandButtonControl class

El control CommandButton ejecuta una macro que realiza una acción cuando un usuario hace clic en ella.

```csharp
public class CommandButtonControl : Forms2OleControl
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CommandButtonControl](commandbuttoncontrol/)() | Inicializa una nueva instancia de`CommandButtonControl` clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Obtiene o establece un color de fondo del control. El valor predeterminado depende del tipo de control. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Obtiene o establece una propiedad Caption del control. El valor predeterminado es una cadena vacía. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Obtiene la colección de controles secundarios inmediatos. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Devuelve`verdadero` si el control está en estado habilitado. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Obtiene o establece un color de primer plano del control. El valor predeterminado depende del tipo de control. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Obtiene o establece una cadena que especifica un grupo de controles mutuamente excluyentes. El valor predeterminado es una cadena vacía. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Obtiene o establece una altura del control en puntos. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Devuelve`verdadero` Si el control es un[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Obtiene o establece el nombre del control ActiveX. |
| override [Type](../../aspose.words.drawing.ole/commandbuttoncontrol/type/) { get; } | Obtiene el tipo de control de Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Obtiene la propiedad Valor subyacente que a menudo representa el estado del control. Por ejemplo, el botón de opción marcado tiene el valor '1' mientras que el desmarcado tiene el valor '0'. El valor predeterminado es una cadena vacía. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Obtiene o establece el ancho del control en puntos. |

## Ejemplos

Muestra cómo insertar un control ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Ver también

* class [Forms2OleControl](../forms2olecontrol/)
* espacio de nombres [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* asamblea [Aspose.Words](../../)
