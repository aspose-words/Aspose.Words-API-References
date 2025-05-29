---
title: FieldChar.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad FieldChar IsDirty ayuda a mantener la precisión del documento mediante el seguimiento de los cambios, garantizando que sus campos siempre reflejen las últimas actualizaciones.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldchar/isdirty/
---
## FieldChar.IsDirty property

Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas al documento.

```csharp
public bool IsDirty { get; set; }
```

## Ejemplos

Muestra cómo trabajar con un nodo FieldStart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Recupera el objeto de fachada que representa el campo en el documento.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

//Actualiza el campo para mostrar la fecha actual.
field.Update();
```

### Ver también

* class [FieldChar](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
