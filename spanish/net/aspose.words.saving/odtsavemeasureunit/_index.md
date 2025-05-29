---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.OdtSaveMeasureUnit para un control preciso de las medidas de sus documentos. ¡Mejore el formato de sus documentos fácilmente!
type: docs
weight: 6100
url: /es/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Unidades de medida especificadas que se aplicarán al contenido medible del documento, como forma, ancho y otros, durante el guardado.

```csharp
public enum OdtSaveMeasureUnit
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Centimeters | `0` | Especifica que el contenido del documento se guarda en centímetros. |
| Inches | `1` | Especifica que el contenido del documento se guarda en pulgadas. |

## Ejemplos

Muestra cómo utilizar diferentes unidades de medida para definir parámetros de estilo de un documento ODT guardado.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Cuando exportamos el documento a .odt, podemos usar un objeto OdtSaveOptions para modificar la forma en que guardamos el documento.
// Podemos establecer la propiedad "MeasureUnit" en "OdtSaveMeasureUnit.Centimeters"
 // para definir contenido como parámetros de estilo utilizando el sistema métrico, que utiliza Open Office.
// Podemos establecer la propiedad "MeasureUnit" en "OdtSaveMeasureUnit.Inches"
// para definir contenido como parámetros de estilo utilizando el sistema imperial, que utiliza Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
