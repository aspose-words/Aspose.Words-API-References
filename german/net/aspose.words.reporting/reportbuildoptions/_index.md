---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Optionen der Aspose.Words ReportingEngine für effizientes Reporting. Passen Sie Ihre Berichte mit flexiblen Einstellungen für optimale Ergebnisse an.
type: docs
weight: 5460
url: /de/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

Gibt Optionen an, die das Verhalten von[`ReportingEngine`](../reportingengine/) während der Erstellung eines Berichts.

```csharp
[Flags]
public enum ReportBuildOptions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Gibt Standardoptionen an. |
| AllowMissingMembers | `1` | Gibt an, dass fehlende Objektelemente von der Engine als Nullliterale behandelt werden sollen. Diese Option betrifft nur den Zugriff auf Instanzobjektelemente (d. h. nicht statische Objektelemente) und Erweiterungsmethoden. Wenn diese Option nicht gesetzt ist, löst die Engine bei einem fehlenden Objektelement eine Exception aus. |
| RemoveEmptyParagraphs | `2` | Gibt an, dass die Engine Absätze entfernen soll, die leer werden, nachdem die Syntax-Tags der Vorlage entfernt oder durch leere Werte ersetzt wurden. |
| InlineErrorMessages | `4` | Gibt an, dass die Engine Fehlermeldungen zur Vorlagensyntax in die Ausgabedokumente einbinden soll. Ist diese Option nicht aktiviert, löst die Engine bei einem Syntaxfehler eine Exception aus. |
| UseLegacyHeaderFooterVisiting | `8` | Gibt an, dass die Engine die untergeordneten Abschnittsknoten (Kopf-, Fuß- und Textteile) in einer Reihenfolge besuchen soll, die mit Aspose.Words-Versionen vor 21.9 kompatibel ist. |
| RespectJpegExifOrientation | `10` | Gibt an, dass die Engine EXIF-Bildorientierungswerte verwenden soll, um eingefügte JPEG-Bilder entsprechend zu drehen. |
| UpdateFieldsSyntaxAware | `20` | Gibt an, dass die Engine die Vorlagensyntax in Feldergebnissen ignorieren und Felder aktualisieren soll, nachdem ein Bericht erstellt wurde. |

### Siehe auch

* namensraum [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Montage [Aspose.Words](../../)
