---
title: RevisionOptions.MeasurementUnit
linktitle: MeasurementUnit
articleTitle: MeasurementUnit
second_title: Aspose.Words para .NET
description: Personaliza tus comentarios de revisión con la propiedad MeasurementUnit de RevisionOptions. Define fácilmente las unidades de medida, con centímetros como valor predeterminado.
type: docs
weight: 80
url: /es/net/aspose.words.layout/revisionoptions/measurementunit/
---
## RevisionOptions.MeasurementUnit property

Permite especificar las unidades de medida para los comentarios de revisión. El valor predeterminado esCentimeters

```csharp
public MeasurementUnits MeasurementUnit { get; set; }
```

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

* enum [MeasurementUnits](../../../aspose.words/measurementunits/)
* class [RevisionOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
