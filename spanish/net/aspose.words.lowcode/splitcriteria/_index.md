---
title: SplitCriteria Enum
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.LowCode.SplitCriteria para una división eficiente de documentos. Optimice su flujo de trabajo con opciones versátiles para una gestión fluida de las piezas.
type: docs
weight: 4400
url: /es/net/aspose.words.lowcode/splitcriteria/
---
## SplitCriteria enumeration

Especifica cómo se divide el documento en partes.

```csharp
public enum SplitCriteria
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Page | `0` | Especifica que el documento está dividido en páginas. |
| SectionBreak | `1` | Especifica que el documento se divide en partes en un salto de sección de cualquier tipo. |
| Style | `2` | Especifica que el documento se divide en partes en un párrafo formateado utilizando el estilo especificado en[`SplitStyle`](../splitoptions/splitstyle/) . |

## Ejemplos

Muestra cómo dividir el documento por páginas.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Ver también

* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
