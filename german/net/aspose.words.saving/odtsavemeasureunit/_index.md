---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.OdtSaveMeasureUnit für präzise Kontrolle über Dokumentmaße. Verbessern Sie mühelos die Formatierung Ihrer Dokumente!
type: docs
weight: 6100
url: /de/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Angegebene Maßeinheiten, die beim Speichern auf messbare Dokumentinhalte wie Form, Breite und andere angewendet werden.

```csharp
public enum OdtSaveMeasureUnit
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Centimeters | `0` | Gibt an, dass der Dokumentinhalt in Zentimetern gespeichert wird. |
| Inches | `1` | Gibt an, dass der Dokumentinhalt in Zoll gespeichert wird. |

## Beispiele

Zeigt, wie verschiedene Maßeinheiten verwendet werden, um Stilparameter eines gespeicherten ODT-Dokuments zu definieren.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Wenn wir das Dokument in .odt exportieren, können wir ein OdtSaveOptions-Objekt verwenden, um zu ändern, wie wir das Dokument speichern.
// Wir können die Eigenschaft „MeasureUnit“ auf „OdtSaveMeasureUnit.Centimeters“ setzen.
    // um Inhalte wie Stilparameter mithilfe des metrischen Systems zu definieren, das Open Office verwendet.
// Wir können die Eigenschaft „MeasureUnit“ auf „OdtSaveMeasureUnit.Inches“ setzen.
// um Inhalte wie Stilparameter mithilfe des imperialen Systems zu definieren, das von Microsoft Word verwendet wird.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
