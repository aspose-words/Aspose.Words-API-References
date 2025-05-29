---
title: MeasurementUnits Enum
linktitle: MeasurementUnits
articleTitle: MeasurementUnits
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.MeasurementUnits para una selección precisa de unidades en el procesamiento de documentos. ¡Mejore su flujo de trabajo con opciones de medición precisas!
type: docs
weight: 4840
url: /es/net/aspose.words/measurementunits/
---
## MeasurementUnits enumeration

Especifica la unidad de medida.

```csharp
public enum MeasurementUnits
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Inches | `0` | Pulgadas. |
| Centimeters | `1` | Centímetros. |
| Millimeters | `2` | Milímetros. |
| Points | `3` | Puntos. |
| Picas | `4` | Picas (comúnmente usado en el espaciado de fuentes de máquinas de escribir tradicionales). |

## Ejemplos

Muestra cómo hacer que un documento guardado se ajuste a un esquema ODT antiguo.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
