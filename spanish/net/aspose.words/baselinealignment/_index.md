---
title: Enum BaselineAlignment
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.BaselineAlignment enumeración. Especifica la posición vertical de las fuentes en una línea.
type: docs
weight: 20
url: /es/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

Especifica la posición vertical de las fuentes en una línea.

```csharp
public enum BaselineAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Top | `0` | Se alinea a lo largo de la parte superior de cada fuente. |
| Center | `1` | Alinea los puntos centrales de cada fuente. |
| Baseline | `2` | Se alinea con la línea base del párrafo. |
| Bottom | `3` | Se alinea con la parte inferior de cada fuente. |
| Auto | `4` | La línea base se ajusta automáticamente. |

### Ejemplos

Muestra cómo configurar la posición vertical de las fuentes en una línea.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


