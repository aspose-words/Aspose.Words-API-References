---
title: Enum OdtSaveMeasureUnit
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.OdtSaveMeasureUnit enumeración. Unidades de medida especificadas para aplicar al contenido medible del documento como la forma el ancho y otros durante el guardado.
type: docs
weight: 5040
url: /es/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Unidades de medida especificadas para aplicar al contenido medible del documento, como la forma, el ancho y otros, durante el guardado.

```csharp
public enum OdtSaveMeasureUnit
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Centimeters | `0` | Especifica que el contenido del documento se guarda usando centímetros. |
| Inches | `1` | Especifica que el contenido del documento se guarda usando pulgadas. |

### Ejemplos

Muestra cómo utilizar diferentes unidades de medida para definir los parámetros de estilo de un documento ODT guardado.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Cuando exportamos el documento a .odt, podemos usar un objeto OdtSaveOptions para modificar cómo guardamos el documento.
// Podemos establecer la propiedad "MeasureUnit" en "OdtSaveMeasureUnit.Centimeters"
// para definir contenido como parámetros de estilo usando el sistema métrico, que usa Open Office. 
// Podemos establecer la propiedad "MeasureUnit" en "OdtSaveMeasureUnit.Inches"
// para definir contenido como parámetros de estilo usando el sistema imperial, que usa Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


