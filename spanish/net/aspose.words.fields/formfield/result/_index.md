---
title: FormField.Result
second_title: Referencia de API de Aspose.Words para .NET
description: FormField propiedad. Obtiene o establece una cadena que representa el resultado de este campo de formulario.
type: docs
weight: 170
url: /es/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

Obtiene o establece una cadena que representa el resultado de este campo de formulario.

```csharp
public string Result { get; set; }
```

### Observaciones

Para un campo de formulario de texto, el resultado es el texto que está en el campo.

Para un campo de formulario de casilla de verificación, el resultado puede ser "1" o "0" para indicar que está marcado o no.

Para un campo de formulario desplegable, el resultado es la cadena seleccionada en el menú desplegable.

Ajuste`Result` para un campo de formulario de texto no se aplica el formato de texto especificado en[`TextInputFormat`](../textinputformat/) . Si desea establecer un valor y aplicar el formato , use el[`SetTextInputValue`](../settextinputvalue/) método.

Para un campo de formulario de texto, el[`TextInputDefault`](../textinputdefault/) el valor se aplica si*value* es`nulo`.

### Ejemplos

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

// El campo del formulario aparecerá en forma de una etiqueta html "seleccionar".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Ver también

* class [FormField](../)
* espacio de nombres [Aspose.Words.Fields](../../formfield/)
* asamblea [Aspose.Words](../../../)


