---
title: XlsxSaveOptions.DateTimeParsingMode
linktitle: DateTimeParsingMode
articleTitle: DateTimeParsingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die DateTimeParsingMode-Eigenschaft von XlsxSaveOptions, um die Art und Weise anzupassen, wie Ihr Dokument Datums- und Uhrzeitangaben analysiert, und so eine genaue Dateninterpretation sicherzustellen.
type: docs
weight: 30
url: /de/net/aspose.words.saving/xlsxsaveoptions/datetimeparsingmode/
---
## XlsxSaveOptions.DateTimeParsingMode property

Ruft den Modus ab oder legt ihn fest, der angibt, wie Dokumenttext analysiert wird, um Datums- und Zeitwerte zu identifizieren. Der Standardwert istUseCurrentLocale .

```csharp
public XlsxDateTimeParsingMode DateTimeParsingMode { get; set; }
```

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

* enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* class [XlsxSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
