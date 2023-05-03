---
title: OdtSaveOptions.IsStrictSchema11
linktitle: IsStrictSchema11
second_title: Aspose.Words for .NET API Reference
description: OdtSaveOptions IsStrictSchema11 property. Specifies whether export should correspond to ODT specification 1.1 strictly. OOo 3.0 displays files correctly when they contain elements and attributes of ODT 1.2. Use false for this purpose or true for strict conformity of specification 1.1. The default value is false in C#.
type: docs
weight: 20
url: /net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Specifies whether export should correspond to ODT specification 1.1 strictly. OOo 3.0 displays files correctly when they contain elements and attributes of ODT 1.2. Use "false" for this purpose, or "true" for strict conformity of specification 1.1. The default value is `false`.

```csharp
public bool IsStrictSchema11 { get; set; }
```

## Examples

Shows how to make a saved document conform to an older ODT schema.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### See Also

* class [OdtSaveOptions](../)
* namespace [Aspose.Words.Saving](../../odtsaveoptions/)
* assembly [Aspose.Words](../../../)
