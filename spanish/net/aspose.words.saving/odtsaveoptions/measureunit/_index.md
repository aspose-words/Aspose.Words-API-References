---
title: OdtSaveOptions.MeasureUnit
second_title: Referencia de API de Aspose.Words para .NET
description: OdtSaveOptions propiedad. Permite especificar unidades de medida para aplicar al contenido del documento. El valor predeterminado esCentimeters
type: docs
weight: 30
url: /es/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Permite especificar unidades de medida para aplicar al contenido del documento. El valor predeterminado esCentimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

### Observaciones

Open Office usa centímetros al especificar longitudes, anchos y otros formatos medibles y propiedades de contenido en documentos, mientras que MS Office usa pulgadas.

### Ejemplos

Muestra cómo utilizar diferentes unidades de medida para definir parámetros de estilo de un documento ODT guardado.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Cuando exportamos el documento a .odt, podemos usar un objeto OdtSaveOptions para modificar cómo guardamos el documento.
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

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../odtsaveoptions/)
* asamblea [Aspose.Words](../../../)


