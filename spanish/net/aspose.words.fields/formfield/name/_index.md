---
title: FormField.Name
second_title: Referencia de API de Aspose.Words para .NET
description: FormField propiedad. Obtiene o establece el nombre del campo de formulario.
type: docs
weight: 130
url: /es/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

Obtiene o establece el nombre del campo de formulario.

```csharp
public string Name { get; set; }
```

### Observaciones

Microsoft Word permite cadenas con un máximo de 20 caracteres.

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


