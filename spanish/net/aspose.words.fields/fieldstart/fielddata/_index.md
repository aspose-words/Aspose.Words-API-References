---
title: FieldStart.FieldData
second_title: Referencia de API de Aspose.Words para .NET
description: FieldStart propiedad. Obtiene datos de campo personalizados asociados con el campo.
type: docs
weight: 10
url: /es/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Obtiene datos de campo personalizados asociados con el campo.

```csharp
public byte[] FieldData { get; }
```

### Ejemplos

Muestra cómo obtener datos asociados con el campo.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.Default.GetString(field.Start.FieldData));
```

### Ver también

* class [FieldStart](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldstart/)
* asamblea [Aspose.Words](../../../)


