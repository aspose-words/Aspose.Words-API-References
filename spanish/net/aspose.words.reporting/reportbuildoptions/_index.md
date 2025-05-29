---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words para .NET
description: Descubra las opciones de Aspose.Words ReportingEngine para crear informes eficientemente. Personalice sus informes con configuraciones flexibles para obtener resultados óptimos.
type: docs
weight: 5460
url: /es/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

Especifica las opciones que controlan el comportamiento de[`ReportingEngine`](../reportingengine/) mientras construía un informe.

```csharp
[Flags]
public enum ReportBuildOptions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Especifica las opciones predeterminadas. |
| AllowMissingMembers | `1` | Especifica que el motor debe tratar los miembros de objeto faltantes como literales nulos. Esta opción afecta únicamente al acceso a miembros de objeto de instancia (es decir, no estáticos) y métodos de extensión. Si no se configura, el motor genera una excepción al detectar un miembro de objeto faltante. |
| RemoveEmptyParagraphs | `2` | Especifica que el motor debe eliminar los párrafos que quedan vacíos después de que las etiquetas de sintaxis de plantilla se eliminan o se reemplazan con valores vacíos. |
| InlineErrorMessages | `4` | Especifica que el motor debe incorporar mensajes de error de sintaxis de plantilla en los documentos de salida. Si esta opción no está configurada, el motor genera una excepción cuando encuentra un error de sintaxis. |
| UseLegacyHeaderFooterVisiting | `8` | Especifica que el motor debe visitar los nodos secundarios de la sección (encabezados, pies de página, cuerpos) en un orden compatible con las versiones de Aspose.Words anteriores a la 21.9. |
| RespectJpegExifOrientation | `10` | Especifica que el motor debe usar valores de orientación de imagen EXIF ​​para rotar adecuadamente las imágenes JPEG insertadas. |
| UpdateFieldsSyntaxAware | `20` | Especifica que el motor debe ignorar la sintaxis de la plantilla en los resultados de campo y actualizar los campos después de que se genere un informe . |

### Ver también

* espacio de nombres [Aspose.Words.Reporting](../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../)
