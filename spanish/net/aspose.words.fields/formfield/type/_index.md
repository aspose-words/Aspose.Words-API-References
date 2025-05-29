---
title: FormField.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubra la propiedad Tipo FormField para identificar y utilizar fácilmente varios tipos de campos de formulario, mejorando la funcionalidad de sus formularios web y la experiencia del usuario.
type: docs
weight: 220
url: /es/net/aspose.words.fields/formfield/type/
---
## FormField.Type property

Devuelve el tipo de campo de formulario.

```csharp
public FieldType Type { get; }
```

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

* enum [FieldType](../../fieldtype/)
* class [FormField](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
