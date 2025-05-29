---
title: XlsxSaveOptions.SectionMode
linktitle: SectionMode
articleTitle: SectionMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SectionMode-Eigenschaft von XlsxSaveOptions die Abschnittsverwaltung für XLSX-Exporte optimiert und so eine nahtlose Dokumentenverwaltung und mehrere Arbeitsblätter gewährleistet.
type: docs
weight: 50
url: /de/net/aspose.words.saving/xlsxsaveoptions/sectionmode/
---
## XlsxSaveOptions.SectionMode property

Ruft ab oder legt fest, wie Abschnitte beim Speichern im XLSX-Ausgabedokument behandelt werden. Der Standardwert istMultipleWorksheets .

```csharp
public XlsxSectionMode SectionMode { get; set; }
```

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

* enum [XlsxSectionMode](../../xlsxsectionmode/)
* class [XlsxSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
