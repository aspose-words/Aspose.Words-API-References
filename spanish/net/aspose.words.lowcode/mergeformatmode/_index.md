---
title: MergeFormatMode Enum
linktitle: MergeFormatMode
articleTitle: MergeFormatMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.LowCode.MergeFormatMode para optimizar la fusión de documentos. Mejore el control de formato al combinar varios archivos sin esfuerzo.
type: docs
weight: 4290
url: /es/net/aspose.words.lowcode/mergeformatmode/
---
## MergeFormatMode enumeration

Especifica cómo se fusiona el formato al combinar varios documentos.

```csharp
public enum MergeFormatMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| MergeFormatting | `0` | Combinar el formato de los documentos fusionados. |
| KeepSourceFormatting | `1` | Significa que el documento fuente conservará su formato original, como estilos de fuente, tamaños, colores, sangrías y cualquier otro elemento de formato aplicado a su contenido. |
| KeepSourceLayout | `2` | Conservar el diseño de los documentos originales en el documento final. |

## Ejemplos

Muestra cómo fusionar documentos en un único documento de salida.

```csharp
//Hay varias formas de fusionar documentos:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
