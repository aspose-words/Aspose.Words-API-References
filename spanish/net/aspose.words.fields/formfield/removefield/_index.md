---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: Aspose.Words para .NET
description: Elimine sin esfuerzo campos de formulario completos con el método FormField RemoveField, mejorando la claridad y la organización de su documento.
type: docs
weight: 240
url: /es/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Elimina el campo de formulario completo, no sólo el carácter especial del campo de formulario.

```csharp
public void RemoveField()
```

## Observaciones

Si hay un marcador asociado al campo de formulario, el marcador no se elimina.

## Ejemplos

Muestra cómo eliminar un campo de formulario.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### Ver también

* class [FormField](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
