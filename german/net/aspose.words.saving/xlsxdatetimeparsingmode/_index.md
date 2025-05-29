---
title: XlsxDateTimeParsingMode Enum
linktitle: XlsxDateTimeParsingMode
articleTitle: XlsxDateTimeParsingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die XlsxDateTimeParsingMode-Aufzählung von Aspose.Words für effizientes Parsen von Dokumenttexten. Identifizieren Sie Datums- und Zeitwerte in Ihren Dateien ganz einfach!
type: docs
weight: 6510
url: /de/net/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enumeration

Gibt an, wie Dokumenttext analysiert wird, um Datums- und Zeitwerte zu identifizieren.

```csharp
public enum XlsxDateTimeParsingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| UseCurrentLocale | `0` | Das für den aktuellen Thread festgelegte Datums-/Uhrzeitformat wird zuerst zum Parsen von Zeichenfolgenwerten verwendet. Schlägt die Analyse fehl, werden andere gängige Datums-/Uhrzeitformate ausprobiert. |
| Auto | `1` | Das im Dokument verwendete Datums-/Uhrzeitformat wird automatisch ermittelt. Dies kann zusätzliche Zeit in Anspruch nehmen. |

## Beispiele

Zeigt, wie die automatische Erkennung des Datums- und Uhrzeitformats angegeben wird.

```csharp
Document doc = new Document(MyDir + "Xlsx DateTime.docx");

XlsxSaveOptions saveOptions = new XlsxSaveOptions();
// Angeben unter Verwendung der automatischen Erkennung des Datums-/Uhrzeitformats.
saveOptions.DateTimeParsingMode = XlsxDateTimeParsingMode.Auto;

doc.Save(ArtifactsDir + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
