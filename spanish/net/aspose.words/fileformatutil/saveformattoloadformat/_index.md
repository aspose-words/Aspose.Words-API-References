---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: Aspose.Words para .NET
description: Convierte fácilmente SaveFormat a LoadFormat con el método FileFormatUtil. ¡Simplifica la gestión de archivos y mejora la compatibilidad hoy mismo!
type: docs
weight: 90
url: /es/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Convierte un[`SaveFormat`](../../saveformat/) valor para un[`LoadFormat`](../../loadformat/) valor si es posible.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentException | Se lanza cuando no se puede convertir. |

## Ejemplos

Muestra cómo convertir un formato de guardado a su formato de carga correspondiente.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Algunos tipos de archivos pueden tener documentos guardados, pero no cargados desde Aspose.Words.
// Si intentamos convertir un formato de guardado de dicho tipo a un formato de carga, se lanzará una excepción.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Ver también

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
