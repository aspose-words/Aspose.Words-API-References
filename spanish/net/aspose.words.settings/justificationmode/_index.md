---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words para .NET
description: Aspose.Words.Settings.JustificationMode enumeración. Especifica el ajuste de espaciado de caracteres para un documento. El valor predeterminado esExpandir  en C#.
type: docs
weight: 5800
url: /es/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Especifica el ajuste de espaciado de caracteres para un documento. El valor predeterminado es`Expandir` .

```csharp
public enum JustificationMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Expand | `0` |  |
| Compress | `1` |  |
| CompressKana | `2` |  |

## Ejemplos

Muestra cómo gestionar el control de espaciado entre caracteres.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)                
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
