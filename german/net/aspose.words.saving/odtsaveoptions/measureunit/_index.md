---
title: OdtSaveOptions.MeasureUnit
second_title: Aspose.Words für .NET-API-Referenz
description: OdtSaveOptions eigendom. Ermöglicht die Angabe von Maßeinheiten die auf den Dokumentinhalt angewendet werden sollen. Der Standardwert istCentimeters
type: docs
weight: 30
url: /de/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Ermöglicht die Angabe von Maßeinheiten, die auf den Dokumentinhalt angewendet werden sollen. Der Standardwert istCentimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

### Bemerkungen

Open Office verwendet Zentimeter, wenn Längen, Breiten und andere messbare Formatierungen und Inhaltseigenschaften in Dokumenten angegeben werden, während MS Office Zoll verwendet.

### Beispiele

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

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../odtsaveoptions/)
* Montage [Aspose.Words](../../../)


