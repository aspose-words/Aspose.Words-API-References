---
title: NumSpacing Enum
linktitle: NumSpacing
articleTitle: NumSpacing
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.NumSpacing para personalizar el espaciado numérico y mejorar el formato de sus documentos. ¡Mejore su presentación de texto hoy mismo!
type: docs
weight: 5030
url: /es/net/aspose.words/numspacing/
---
## NumSpacing enumeration

Especifica los valores posibles en los que se puede mostrar el espaciado numérico.

```csharp
public enum NumSpacing
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Default | `0` | Especifica que los números se muestran en el formato predeterminado de la fuente. |
| Proportional | `1` | Especifica que las formas de los numerales diseñados como espaciados proporcionalmente se mostrarán si la fuente lo admite. |
| Tabular | `2` | Especifica que las formas de los numerales diseñados como tabulares se mostrarán si la fuente lo admite. |

## Ejemplos

Muestra cómo establecer el tipo de espaciado del numeral.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Este efecto solo es compatible con versiones más nuevas de MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
