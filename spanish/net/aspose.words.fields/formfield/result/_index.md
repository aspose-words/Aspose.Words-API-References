---
title: FormField.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words para .NET
description: Descubra la propiedad FormField Result, administre y personalice fácilmente la salida de cadena de sus campos de formulario para una mejor experiencia del usuario.
type: docs
weight: 170
url: /es/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

Obtiene o establece una cadena que representa el resultado de este campo de formulario.

```csharp
public string Result { get; set; }
```

## Observaciones

Para un campo de formulario de texto, el resultado es el texto que está en el campo.

Para un campo de formulario de casilla de verificación, el resultado puede ser "1" o "0" para indicar si está marcado o no.

Para un campo de formulario desplegable, el resultado es la cadena seleccionada en el menú desplegable.

Configuración`Result` para un campo de formulario de texto no se aplica el formato de texto especificado en[`TextInputFormat`](../textinputformat/) Si desea establecer un valor y aplicar el formato , utilice el[`SetTextInputValue`](../settextinputvalue/) método.

Para un campo de formulario de texto, el[`TextInputDefault`](../textinputdefault/) El valor se aplica si*value* es`nulo`.

## Ejemplos

Muestra cómo insertar un cuadro combinado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Inserte un cuadro combinado que permitirá al usuario elegir una opción de una colección de cadenas.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

//El campo de formulario aparecerá en forma de una etiqueta html "select".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Ver también

* class [FormField](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
