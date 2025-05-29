---
title: OdtSaveOptions.MeasureUnit
linktitle: MeasureUnit
articleTitle: MeasureUnit
second_title: Aspose.Words für .NET
description: Passen Sie die Maßeinheit Ihres Dokuments mit OdtSaveOptions an. Wählen Sie Ihre bevorzugte Maßeinheit für die Genauigkeit – die Standardeinstellung ist Zentimeter.
type: docs
weight: 40
url: /de/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Ermöglicht die Angabe von Maßeinheiten für den Dokumentinhalt. Der Standardwert istCentimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

## Bemerkungen

Open Office verwendet Zentimeter bei der Angabe von Längen, Breiten und anderen messbaren Formatierungs- und Inhaltseigenschaften in Dokumenten, während MS Office Zoll verwendet.

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

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
