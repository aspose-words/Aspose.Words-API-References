---
title: PdfCompliance Enum
linktitle: PdfCompliance
articleTitle: PdfCompliance
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Saving.PdfCompliance para mejorar el cumplimiento de los estándares PDF. ¡Mejore la calidad de sus documentos con opciones personalizadas para cada necesidad!
type: docs
weight: 6200
url: /es/net/aspose.words.saving/pdfcompliance/
---
## PdfCompliance enumeration

Especifica el nivel de cumplimiento de los estándares PDF.

```csharp
public enum PdfCompliance
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Pdf17 | `0` | El archivo de salida cumplirá con el estándar PDF 1.7 (ISO 32000-1). |
| Pdf20 | `1` | El archivo de salida cumplirá con el estándar PDF 2.0 (ISO 32000-2). |
| PdfA1a | `2` | El archivo de salida cumplirá con el estándar PDF/A-1a (ISO 19005-1). Este nivel incluye todos los requisitos de PDF/A-1b y, además, requiere que se incluya la estructura del documento (también conocida como "etiquetado"), con el objetivo de garantizar que se pueda buscar y reutilizar el contenido del documento. |
| PdfA1b | `3` | El archivo de salida cumplirá con el estándar PDF/A-1b (ISO 19005-1). PDF/A-1b tiene el objetivo de garantizar una reproducción confiable de la apariencia visual del documento. |
| PdfA2a | `4` | El archivo de salida cumplirá con el estándar PDF/A-2a (ISO 19005-2). Este nivel incluye todos los requisitos de PDF/A-2u y, además, requiere que se incluya la estructura del documento (también conocida como "etiquetado"), con el objetivo de garantizar que se pueda buscar y reutilizar el contenido del documento. |
| PdfA2u | `5` | El archivo de salida cumplirá con el estándar PDF/A-2u (ISO 19005-2). PDF/A-2u tiene como objetivo preservar la apariencia visual estática del documento a lo largo del tiempo, independientemente de las herramientas y sistemas utilizados para crear, almacenar o renderizar los archivos. Además, cualquier texto contenido en el documento se puede extraer de forma fiable como una serie de puntos de código Unicode. |
| PdfA3a | `6` | El archivo de salida cumplirá con el estándar PDF/A-3a (ISO 19005-3). Este nivel incluye todos los requisitos de PDF/A-3u y, además, requiere que se incluya la estructura del documento (también conocida como "etiquetado"), con el objetivo de garantizar que se pueda buscar y reutilizar el contenido del documento. |
| PdfA3u | `7` | El archivo de salida cumple con el estándar PDF/A-3u (ISO 19005-3). PDF/A-3u (al igual que PDF/A-2u) tiene como objetivo preservar la apariencia visual estática del documento a lo largo del tiempo, independientemente de las herramientas y sistemas utilizados para crear, almacenar o renderizar los archivos. Además, cualquier texto contenido en el documento se puede extraer de forma fiable como una serie de puntos de código Unicode. Además de PDF/A-2u, PDF/A-3u permite incrustar archivos adjuntos en el documento PDF. |
| PdfA4 | `8` | El archivo de salida cumplirá con el estándar PDF/A-4 (ISO 19005-4:2020). El objetivo de PDF/A-4 es preservar la apariencia visual estática del documento a lo largo del tiempo, independientemente de las herramientas y sistemas utilizados para crear, almacenar o renderizar los archivos. Además, cualquier texto contenido en el documento se puede extraer de forma fiable como una serie de puntos de código Unicode. |
| PdfA4f | `9` | El archivo de salida cumplirá con el estándar PDF/A-4f (ISO 19005-4:2020). Este nivel incluye todos los requisitos de PDF/A-4 y además permite incrustar archivos adjuntos en el documento PDF. |
| PdfA4Ua2 | `10` | El archivo de salida cumplirá con los estándares PDF/A-4 (ISO 19005-4:2020) y PDF/UA-2 (ISO 14289-2:2024). El objetivo de PDF/A-4 es preservar la apariencia visual estática del documento a lo largo del tiempo, independientemente de las herramientas y sistemas utilizados para crear, almacenar o renderizar los archivos. El propósito principal de PDF/UA es definir cómo representar documentos electrónicos en formato PDF de forma que el archivo sea accesible. |
| PdfUa1 | `11` | El archivo de salida cumplirá con el estándar PDF/UA-1 (ISO 14289-1). El propósito principal de PDF/UA es definir cómo representar documentos electrónicos en formato PDF de una manera que permita que el archivo sea accesible. |
| PdfUa2 | `12` | El archivo de salida cumplirá con el estándar PDF/UA-2 (ISO 14289-2:2024). El propósito principal de PDF/UA es definir cómo representar documentos electrónicos en formato PDF de una manera que permita que el archivo sea accesible. |

## Ejemplos

Muestra cómo establecer el nivel de conformidad con los estándares PDF de los documentos PDF guardados.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
// Tenga en cuenta que algunas PdfSaveOptions están prohibidas al guardar en uno de los estándares y se corrigen automáticamente.
// Utilice IWarningCallback para saber qué opciones se corrigen automáticamente.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establezca la propiedad "Compliance" en "PdfCompliance.PdfA1b" para cumplir con el estándar "PDF/A-1b",
// que tiene como objetivo preservar la apariencia visual del documento mientras Aspose.Words lo convierte a PDF.
// Establezca la propiedad "Compliance" en "PdfCompliance.Pdf17" para cumplir con el estándar "1.7".
// Establezca la propiedad "Compliance" en "PdfCompliance.PdfA1a" para cumplir con el estándar "PDF/A-1a",
// que cumple con "PDF/A-1b" y además conserva la estructura del documento original.
// Establezca la propiedad "Compliance" en "PdfCompliance.PdfUa1" para cumplir con el estándar "PDF/UA-1" (ISO 14289-1),
// que tiene como objetivo definir representar documentos electrónicos en formato PDF que permitan que el archivo sea accesible.
// Establezca la propiedad "Compliance" en "PdfCompliance.Pdf20" para cumplir con el estándar "PDF 2.0" (ISO 32000-2).
// Establezca la propiedad "Compliance" en "PdfCompliance.PdfA4" para cumplir con el estándar "PDF/A-4" (ISO 19004:2020),
// que preserva la apariencia visual estática del documento a lo largo del tiempo.
// Establezca la propiedad "Compliance" en "PdfCompliance.PdfA4Ua2" para cumplir con PDF/A-4 (ISO 19005-4:2020)
// y estándares PDF/UA-2 (ISO 14289-2:2024).
// Establezca la propiedad "Compliance" en "PdfCompliance.PdfUa2" para cumplir con el estándar PDF/UA-2 (ISO 14289-2:2024).
// Esto ayuda a que los documentos se puedan buscar, pero puede aumentar significativamente el tamaño de documentos que ya son grandes.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
