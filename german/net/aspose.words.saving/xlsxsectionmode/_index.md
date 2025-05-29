---
title: XlsxSectionMode Enum
linktitle: XlsxSectionMode
articleTitle: XlsxSectionMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Aufzählung Aspose.Words XlsxSectionMode das Speichern von Dokumenten im XLSX-Format optimiert und so Ihren Arbeitsablauf und Ihr Dokumentenmanagement verbessert.
type: docs
weight: 6530
url: /de/net/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enumeration

Gibt an, wie Abschnitte beim Speichern eines Dokuments im XLSX-Format behandelt werden.

```csharp
public enum XlsxSectionMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| MultipleWorksheets | `0` | Gibt an, dass für jeden Abschnitt eines Dokuments ein separates Arbeitsblatt erstellt wird. |
| SingleWorksheet | `1` | Gibt an, dass alle Abschnitte eines Dokuments auf einem Arbeitsblatt gespeichert werden. |

## Beispiele

Zeigt, wie Dokumente als separate Arbeitsblätter gespeichert werden.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Jeder Abschnitt eines Dokuments wird als separates Arbeitsblatt erstellt.
// Verwenden Sie „SingleWorksheet“, um alle Dokumente auf einem Arbeitsblatt anzuzeigen.
XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.SectionMode = XlsxSectionMode.MultipleWorksheets;

doc.Save(ArtifactsDir + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
