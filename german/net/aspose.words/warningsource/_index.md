---
title: WarningSource Enum
linktitle: WarningSource
articleTitle: WarningSource
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.WarningSource, die Warnquellen beim Laden und Speichern von Dokumenten identifiziert und so die Dokumentenverwaltung verbessert.
type: docs
weight: 7500
url: /de/net/aspose.words/warningsource/
---
## WarningSource enumeration

Gibt das Modul an, das beim Laden oder Speichern eines Dokuments eine Warnung ausgibt.

```csharp
public enum WarningSource
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Unknown | `0` | Die Warnungsquelle ist nicht angegeben. |
| Layout | `1` | Modul, das ein Dokumentlayout erstellt. |
| DrawingML | `2` | Modul, das DrawingML-Formen rendert. |
| OfficeMath | `3` | Modul, das OfficeMath rendert. |
| Shapes | `4` | Modul, das gewöhnliche Formen rendert. |
| Metafile | `5` | Modul zum Rendern von Metadateien. |
| Xps | `6` | Modul, das XPS rendert. |
| Pdf | `7` | Modul zum Rendern von PDF. |
| Image | `8` | Modul zum Rendern von Bildern. |
| Docx | `9` | Modul zum Lesen/Schreiben von DOCX-Dateien. |
| Doc | `10` | Modul zum Lesen/Schreiben binärer DOC-Dateien. |
| Text | `11` | Modul zum Lesen/Schreiben von Klartextdateien. |
| Rtf | `12` | Modul zum Lesen/Schreiben von RTF-Dateien. |
| WordML | `13` | Modul zum Lesen/Schreiben von WML-Dateien. |
| Nrx | `14` | Gemeinsame Module, die von DOCX/WML-Lese-/Schreibmodulen gemeinsam genutzt werden. |
| Odt | `15` | Modul zum Lesen/Schreiben von ODT-Dateien. |
| Html | `16` | Modul zum Lesen/Schreiben von HTML/MHTML-Dateien. |
| Validator | `17` | Modul, das die Konsistenz und Gültigkeit des Modells überprüft. |
| Xaml | `18` | Modul, das XAML-Dateien liest/schreibt. |
| Svm | `19` | Modul, das SVM-Dateien liest. |
| MathML | `20` | Modul, das W3C MathML-Dateien liest. |
| Font | `21` | Modul zum Lesen von Schriftdateien. |
| Svg | `22` | Modul, das SVG-Dateien liest. |
| Markdown | `23` | Modul, das Markdown-Dateien liest/schreibt. |
| Chm | `24` | Modul, das CHM-Dateien liest. |
| Epub | `25` | Modul zum Lesen/Schreiben von EPUB-Dateien. |
| Xml | `26` | Modul zum Lesen von XML-Dateien. |
| Xlsx | `27` | Modul zum Schreiben von XLSX-Dateien. |

## Beispiele

Zeigt, wie mit der Warnquelle gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
