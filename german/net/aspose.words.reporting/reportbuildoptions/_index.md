---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.Reporting.ReportBuildOptions opsomming. Gibt Optionen an die das Verhalten von steuernReportingEngine beim Erstellen eines Berichts in C#.
type: docs
weight: 4720
url: /de/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

Gibt Optionen an, die das Verhalten von steuern[`ReportingEngine`](../reportingengine/) beim Erstellen eines Berichts.

```csharp
[Flags]
public enum ReportBuildOptions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Gibt Standardoptionen an. |
| AllowMissingMembers | `1` | Gibt an, dass fehlende Objektmitglieder von der Engine als Nullliterale behandelt werden sollen. Diese Option betrifft nur den Zugriff auf Instanzobjektmitglieder (d. h. nicht statische Objekte) und Erweiterungsmethoden. Wenn diese Option nicht festgelegt ist, löst die Engine eine Ausnahme aus, wenn sie auf ein fehlendes Objektmitglied stößt. |
| RemoveEmptyParagraphs | `2` | Gibt an, dass die Engine leer werdende Absätze entfernen soll, nachdem Vorlagensyntax-Tags entfernt oder durch leere Werte ersetzt wurden. |
| InlineErrorMessages | `4` | Gibt an, dass die Engine Fehlermeldungen zur Vorlagensyntax in Ausgabedokumente integrieren soll. Wenn diese Option nicht gesetzt ist, löst die Engine eine Ausnahme aus, wenn ein Syntaxfehler auftritt. |
| UseLegacyHeaderFooterVisiting | `8` | Gibt an, dass die Engine untergeordnete Abschnittsknoten (Kopfzeilen, Fußzeilen, Körper) in einer Reihenfolge besuchen soll , die mit Aspose.Words-Versionen vor 21.9. kompatibel ist. |
| RespectJpegExifOrientation | `10` | Gibt an, dass die Engine EXIF-Bildausrichtungswerte verwenden soll, um eingefügte JPEG-Bilder entsprechend zu drehen. |

### Siehe auch

* namensraum [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Montage [Aspose.Words](../../)
