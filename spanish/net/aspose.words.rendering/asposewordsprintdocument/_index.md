---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words para .NET
description: Aspose.Words.Rendering.AsposeWordsPrintDocument clase. Proporciona una implementación predeterminada para la impresión de unDocument inside el marco de impresión .NET en C#.
type: docs
weight: 4530
url: /es/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Proporciona una implementación predeterminada para la impresión de un[`Document`](../../aspose.words/document/) inside el marco de impresión .NET.

Para obtener más información, visite el[Imprimir un documento mediante programación o mediante cuadros de diálogo](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) artículo de documentación.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Obtiene o establece cómo se imprimen las páginas sin color si el dispositivo admite la impresión en color. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Obtiene el número de páginas impresas en color (es decir, conColor establecido en verdadero). |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Lee y almacena en caché algunos campos dePrinterSettings para reducir el tiempo de impresión. |

## Observaciones

`AsposeWordsPrintDocument` anulaPrintEventArgs) para imprimir el rango de páginas que se especifica enPrinterSettings.

Un solo documento de Word puede constar de varias secciones que especifican páginas con diferentes tamaños, orientación y bandejas de papel.`AsposeWordsPrintDocument` anulaciones QueryPageSettingsEventArgs) para seleccionar correctamente el tamaño del papel, la orientación y el origen del papel al imprimir un documento de Word.

Microsoft Word almacena valores específicos de la impresora para las bandejas de papel en un documento de Word y, por lo tanto, solo imprimir en el mismo modelo de impresora que se seleccionó cuando el usuario especificó las bandejas de papel dará como resultado la impresión desde las bandejas correctas. Si imprime un documento en una impresora diferente, lo más probable es que se utilice la bandeja de papel predeterminada, no las bandejas especificadas en el documento.

### Ver también

* espacio de nombres [Aspose.Words.Rendering](../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../)
