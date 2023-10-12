---
title: OdtSaveOptions.IsStrictSchema11
second_title: Aspose.Words für .NET-API-Referenz
description: OdtSaveOptions eigendom. Gibt an ob der Export strikt der ODTSpezifikation 1.1 entsprechen soll. OOo 3.0 zeigt Dateien korrekt an wenn sie Elemente und Attribute von ODT 1.2 enthalten. Verwenden Sie für diesen Zweck false oder true für strikte Konformität mit der Spezifikation 1.1. Der Standardwert istFALSCH .
type: docs
weight: 20
url: /de/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Gibt an, ob der Export strikt der ODT-Spezifikation 1.1 entsprechen soll. OOo 3.0 zeigt Dateien korrekt an, wenn sie Elemente und Attribute von ODT 1.2 enthalten. Verwenden Sie für diesen Zweck „false“ oder „true“ für strikte Konformität mit der Spezifikation 1.1. Der Standardwert ist`FALSCH` .

```csharp
public bool IsStrictSchema11 { get; set; }
```

### Beispiele

Zeigt, wie ein gespeichertes Dokument an ein älteres ODT-Schema angepasst wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Siehe auch

* class [OdtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../odtsaveoptions/)
* Montage [Aspose.Words](../../../)


