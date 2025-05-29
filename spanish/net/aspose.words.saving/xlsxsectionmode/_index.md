---
title: XlsxSectionMode Enum
linktitle: XlsxSectionMode
articleTitle: XlsxSectionMode
second_title: Aspose.Words para .NET
description: Descubra cómo la enumeración XlsxSectionMode de Aspose.Words optimiza el guardado de documentos en formato XLSX, mejorando su flujo de trabajo y la gestión de documentos.
type: docs
weight: 6530
url: /es/net/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enumeration

Especifica cómo se manejan las secciones al guardar un documento en formato XLSX.

```csharp
public enum XlsxSectionMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| MultipleWorksheets | `0` | Especifica que se crea una hoja de cálculo independiente para cada sección de un documento. |
| SingleWorksheet | `1` | Especifica que todas las secciones de un documento se guardan en una hoja de cálculo. |

## Ejemplos

Muestra cómo guardar documentos como hojas de trabajo separadas.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

//Cada sección de un documento se creará como una hoja de trabajo independiente.
// Utilice 'SingleWorksheet' para mostrar todos los documentos en una hoja de trabajo.
XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.SectionMode = XlsxSectionMode.MultipleWorksheets;

doc.Save(ArtifactsDir + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
