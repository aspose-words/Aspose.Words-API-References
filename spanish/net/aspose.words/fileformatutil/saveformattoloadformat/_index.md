---
title: FileFormatUtil.SaveFormatToLoadFormat
second_title: Referencia de API de Aspose.Words para .NET
description: FileFormatUtil método. Convierte unSaveFormat valor a unLoadFormat valor si es posible.
type: docs
weight: 90
url: /es/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Convierte un[`SaveFormat`](../../saveformat/) valor a un[`LoadFormat`](../../loadformat/) valor si es posible.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentException | Lanza cuando no se puede convertir. |

### Ejemplos

Muestra cómo convertir un formato guardado a su formato de carga correspondiente.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Algunos tipos de archivos pueden tener documentos guardados, pero no cargados con Aspose.Words.
// Si intentamos convertir un formato guardado de este tipo a un formato de carga, se lanzará una excepción.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Ver también

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* espacio de nombres [Aspose.Words](../../fileformatutil/)
* asamblea [Aspose.Words](../../../)


