---
title: FormField.RemoveField
second_title: Referencia de API de Aspose.Words para .NET
description: FormField método. Elimina el campo completo del formulario no solo el carácter especial del campo del formulario.
type: docs
weight: 240
url: /es/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Elimina el campo completo del formulario, no solo el carácter especial del campo del formulario.

```csharp
public void RemoveField()
```

### Observaciones

Si hay un marcador asociado con el campo del formulario, el marcador no se elimina.

### Ejemplos

Muestra cómo eliminar un campo de formulario.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### Ver también

* class [FormField](../)
* espacio de nombres [Aspose.Words.Fields](../../formfield/)
* asamblea [Aspose.Words](../../../)


