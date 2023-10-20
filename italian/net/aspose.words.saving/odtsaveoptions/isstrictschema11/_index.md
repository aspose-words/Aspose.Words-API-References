---
title: OdtSaveOptions.IsStrictSchema11
linktitle: IsStrictSchema11
articleTitle: IsStrictSchema11
second_title: Aspose.Words per .NET
description: OdtSaveOptions IsStrictSchema11 proprietà. Specifica se lesportazione deve corrispondere rigorosamente alla specifica ODT 1.1. OOo 3.0 visualizza i file correttamente quando contengono elementi e attributi di ODT 1.2. Utilizzare false per questo scopo o true per la stretta conformità alla specifica 1.1. Il valore predefinito èfalso  in C#.
type: docs
weight: 20
url: /it/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Specifica se l'esportazione deve corrispondere rigorosamente alla specifica ODT 1.1. OOo 3.0 visualizza i file correttamente quando contengono elementi e attributi di ODT 1.2. Utilizzare "false" per questo scopo o "true" per la stretta conformità alla specifica 1.1. Il valore predefinito è`falso` .

```csharp
public bool IsStrictSchema11 { get; set; }
```

## Esempi

Mostra come rendere un documento salvato conforme a uno schema ODT precedente.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Guarda anche

* class [OdtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
