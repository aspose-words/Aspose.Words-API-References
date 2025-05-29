---
title: Underline Enum
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Underline para opciones versátiles de subrayado de fuentes. ¡Mejore el formato de sus documentos con estilos personalizables hoy mismo!
type: docs
weight: 7360
url: /es/net/aspose.words/underline/
---
## Underline enumeration

Indica el tipo de subrayado aplicado a una fuente.

```csharp
public enum Underline
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` |  |
| Single | `1` |  |
| Words | `2` |  |
| Double | `3` |  |
| Dotted | `4` |  |
| Thick | `6` |  |
| Dash | `7` |  |
| DashLong | `39` |  |
| DotDash | `9` |  |
| DotDotDash | `10` |  |
| Wavy | `11` |  |
| DottedHeavy | `20` |  |
| DashHeavy | `23` |  |
| DashLongHeavy | `55` |  |
| DotDashHeavy | `25` |  |
| DotDotDashHeavy | `26` |  |
| WavyHeavy | `27` |  |
| WavyDouble | `43` |  |

## Ejemplos

Muestra cómo insertar un campo de hipervínculo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Inserta un hipervínculo y enfatízalo con formato personalizado.
// El hipervínculo será un fragmento de texto en el que se puede hacer clic y que nos llevará a la ubicación especificada en la URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", falso);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + clic izquierdo en el enlace del texto en Microsoft Word nos llevará a la URL a través de una nueva ventana del navegador web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
