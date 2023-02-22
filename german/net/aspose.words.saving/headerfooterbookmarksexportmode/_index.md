---
title: Enum HeaderFooterBookmarksExportMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.HeaderFooterBookmarksExportMode opsomming. Gibt an wie Lesezeichen in Kopf/Fußzeilen exportiert werden.
type: docs
weight: 4790
url: /de/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

Gibt an, wie Lesezeichen in Kopf-/Fußzeilen exportiert werden.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Lesezeichen in Kopf-/Fußzeilen werden nicht exportiert. |
| First | `1` | Nur das Lesezeichen in der ersten Kopf-/Fußzeile des Abschnitts wird exportiert. |
| All | `2` | Lesezeichen in allen Kopf-/Fußzeilen werden exportiert. |

### Beispiele

Zeigt die Verarbeitung von Lesezeichen in Kopf-/Fußzeilen in einem Dokument an, das wir in PDF rendern.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Legen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseOutlines“ fest, um den Gliederungsnavigationsbereich in der Ausgabe-PDF anzuzeigen.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Setzen Sie die Eigenschaft "DefaultBookmarksOutlineLevel" auf "1", um alles anzuzeigen
// Lesezeichen auf der ersten Gliederungsebene im Ausgabe-PDF.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Legen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.None" fest
// keine Lesezeichen exportieren, die sich in Kopf-/Fußzeilen befinden.
// Legen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.First" fest
// Lesezeichen nur in den Kopf-/Fußzeilen des ersten Abschnitts exportieren.
// Legen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.All" fest
// Lesezeichen exportieren, die sich in allen Kopf-/Fußzeilen befinden.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


