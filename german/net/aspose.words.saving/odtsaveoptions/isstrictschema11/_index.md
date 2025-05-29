---
title: OdtSaveOptions.IsStrictSchema11
linktitle: IsStrictSchema11
articleTitle: IsStrictSchema11
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre ODT-Exporte mit der Eigenschaft IsStrictSchema11. Stellen Sie die strikte Einhaltung von ODT 1.1 sicher oder aktivieren Sie die 1.2-Kompatibilität für optimale Ergebnisse.
type: docs
weight: 30
url: /de/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Gibt an, ob der Export strikt der ODT-Spezifikation 1.1 entsprechen soll. OOo 3.0 zeigt Dateien korrekt an, wenn sie Elemente und Attribute von ODT 1.2 enthalten. Verwenden Sie hierfür "false" oder "true" für strikte Konformität mit Spezifikation 1.1. Der Standardwert ist`FALSCH` .

```csharp
public bool IsStrictSchema11 { get; set; }
```

## Beispiele

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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
