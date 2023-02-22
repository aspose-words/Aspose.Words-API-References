---
title: OdtSaveOptions.IsStrictSchema11
second_title: Aspose.Words per .NET API Reference
description: OdtSaveOptions proprietà. Specifica se lesportazione deve corrispondere rigorosamente alla specifica ODT 1.1. OOo 3.0 visualizza correttamente i file quando contengono elementi e attributi di ODT 1.2. Utilizzare false per questo scopo o true per la stretta conformità alla specifica 1.1. Il valore predefinito è falso .
type: docs
weight: 20
url: /it/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Specifica se l'esportazione deve corrispondere rigorosamente alla specifica ODT 1.1. OOo 3.0 visualizza correttamente i file quando contengono elementi e attributi di ODT 1.2. Utilizzare "false" per questo scopo, o "true" per la stretta conformità alla specifica 1.1. Il valore predefinito è **falso** .

```csharp
public bool IsStrictSchema11 { get; set; }
```

### Esempi

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
* spazio dei nomi [Aspose.Words.Saving](../../odtsaveoptions/)
* assemblea [Aspose.Words](../../../)


