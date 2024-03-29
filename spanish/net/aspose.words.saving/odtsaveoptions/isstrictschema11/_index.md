---
title: OdtSaveOptions.IsStrictSchema11
linktitle: IsStrictSchema11
articleTitle: IsStrictSchema11
second_title: Aspose.Words para .NET
description: OdtSaveOptions IsStrictSchema11 propiedad. Especifica si la exportación debe corresponder estrictamente a la especificación ODT 1.1. OOo 3.0 muestra archivos correctamente cuando contienen elementos y atributos de ODT 1.2. Utilice falso para este propósito o verdadero para conformidad estricta con la especificación 1.1. El valor predeterminado esFALSO  en C#.
type: docs
weight: 20
url: /es/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Especifica si la exportación debe corresponder estrictamente a la especificación ODT 1.1. OOo 3.0 muestra archivos correctamente cuando contienen elementos y atributos de ODT 1.2. Utilice "falso" para este propósito, o "verdadero" para conformidad estricta con la especificación 1.1. El valor predeterminado es`FALSO` .

```csharp
public bool IsStrictSchema11 { get; set; }
```

## Ejemplos

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

* class [OdtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
