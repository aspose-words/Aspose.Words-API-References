---
title: OdtSaveOptions.IsStrictSchema11
linktitle: IsStrictSchema11
articleTitle: IsStrictSchema11
second_title: Aspose.Words för .NET
description: Optimera dina ODT-exporter med egenskapen IsStrictSchema11. Säkerställ strikt efterlevnad av ODT 1.1 eller aktivera 1.2-kompatibilitet för bästa resultat.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Anger om exporten ska överensstämma strikt med ODT-specifikation 1.1. OOo 3.0 visar filer korrekt när de innehåller element och attribut från ODT 1.2. Använd "false" för detta ändamål eller "sant" för strikt överensstämmelse med specifikation 1.1. Standardvärdet är`falsk` .

```csharp
public bool IsStrictSchema11 { get; set; }
```

## Exempel

Visar hur man får ett sparat dokument att överensstämma med ett äldre ODT-schema.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Se även

* class [OdtSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
