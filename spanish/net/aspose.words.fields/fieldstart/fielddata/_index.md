---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words para .NET
description: Desbloquee datos de campos personalizados con la propiedad FieldData de FieldStart, mejorando su gestión de datos y aumentando la productividad sin esfuerzo.
type: docs
weight: 10
url: /es/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Obtiene datos de campo personalizados que están asociados con el campo.

```csharp
public byte[] FieldData { get; }
```

## Ejemplos

Muestra cómo obtener datos asociados con el campo.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.UTF8.GetString(field.Start.FieldData));
```

### Ver también

* class [FieldStart](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
