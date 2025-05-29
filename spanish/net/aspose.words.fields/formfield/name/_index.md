---
title: FormField.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words para .NET
description: Descubra cómo administrar fácilmente la propiedad FormField Name para personalizar y optimizar sus formularios para una mejor participación del usuario y recopilación de datos.
type: docs
weight: 130
url: /es/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

Obtiene o establece el nombre del campo de formulario.

```csharp
public string Name { get; set; }
```

## Observaciones

Microsoft Word permite cadenas con un máximo de 20 caracteres.

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
