---
title: XlsxSaveOptions.SectionMode
linktitle: SectionMode
articleTitle: SectionMode
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad XlsxSaveOptions SectionMode optimiza el manejo de secciones para exportaciones XLSX, lo que garantiza una administración fluida de documentos y múltiples hojas de trabajo.
type: docs
weight: 50
url: /es/net/aspose.words.saving/xlsxsaveoptions/sectionmode/
---
## XlsxSaveOptions.SectionMode property

Obtiene o establece la forma en que se manejan las secciones al guardar en el documento XLSX de salida. El valor predeterminado esMultipleWorksheets .

```csharp
public XlsxSectionMode SectionMode { get; set; }
```

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

* enum [XlsxSectionMode](../../xlsxsectionmode/)
* class [XlsxSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
