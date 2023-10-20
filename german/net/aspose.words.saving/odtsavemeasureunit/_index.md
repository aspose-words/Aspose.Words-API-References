---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.OdtSaveMeasureUnit opsomming. Spezifizierte Maßeinheiten die beim Speichern auf messbare Dokumentinhalte wie Form Breite usw. angewendet werden sollen in C#.
type: docs
weight: 5320
url: /de/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Spezifizierte Maßeinheiten, die beim Speichern auf messbare Dokumentinhalte wie Form, Breite usw. angewendet werden sollen.

```csharp
public enum OdtSaveMeasureUnit
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Centimeters | `0` | Gibt an, dass der Dokumentinhalt in Zentimetern gespeichert wird. |
| Inches | `1` | Gibt an, dass der Dokumentinhalt in Zoll gespeichert wird. |

## Beispiele

Zeigt, wie Sie verschiedene Maßeinheiten verwenden, um Stilparameter eines gespeicherten ODT-Dokuments zu definieren.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Wenn wir das Dokument in .odt exportieren, können wir ein OdtSaveOptions-Objekt verwenden, um zu ändern, wie wir das Dokument speichern.
// Wir können die Eigenschaft „MeasureUnit“ auf „OdtSaveMeasureUnit.Centimeters“ setzen
 // um Inhalte wie Stilparameter mithilfe des metrischen Systems zu definieren, das Open Office verwendet.
// Wir können die Eigenschaft „MeasureUnit“ auf „OdtSaveMeasureUnit.Inches“ setzen.
// um Inhalte wie Stilparameter mithilfe des imperialen Systems zu definieren, das Microsoft Word verwendet.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
