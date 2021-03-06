---
title: IsStrictSchema11
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica si la exportación debe corresponder estrictamente a la especificación 1.1 de ODT. OOo 3.0 muestra los archivos correctamente cuando contienen elementos y atributos de ODT 1.2. Use falso para este propósito o verdadero para conformidad estricta con la especificación 1.1. El valor predeterminado es falso .
type: docs
weight: 20
url: /es/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Especifica si la exportación debe corresponder estrictamente a la especificación 1.1 de ODT. OOo 3.0 muestra los archivos correctamente cuando contienen elementos y atributos de ODT 1.2. Use "falso" para este propósito, o "verdadero" para conformidad estricta con la especificación 1.1. El valor predeterminado es **falso** .

```csharp
public bool IsStrictSchema11 { get; set; }
```

### Ejemplos

Muestra cómo hacer que un documento guardado se ajuste a un esquema ODT anterior.

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

* class [OdtSaveOptions](../../odtsaveoptions)
* espacio de nombres [Aspose.Words.Saving](../../odtsaveoptions)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
