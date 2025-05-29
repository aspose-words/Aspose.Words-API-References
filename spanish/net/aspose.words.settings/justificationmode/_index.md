---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words JustificationMode para ajustar con precisión el espaciado entre caracteres en sus documentos. ¡Mejore la legibilidad con ajustes personalizables!
type: docs
weight: 6630
url: /es/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Especifica el ajuste del espaciado de caracteres para un documento. El valor predeterminado es`Expandir` .

```csharp
public enum JustificationMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Expand | `0` | No comprima el espaciado entre caracteres. |
| Compress | `1` | Comprimir el espaciado entre caracteres. |
| CompressKana | `2` | Comprimir, utilizando reglas de los silabarios kana, hiragana y katakana. |

## Ejemplos

Muestra cómo administrar el control del espaciado entre caracteres.

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
