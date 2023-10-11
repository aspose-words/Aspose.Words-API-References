---
title: Enum HeaderFooterBookmarksExportMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.HeaderFooterBookmarksExportMode opsomming. Gibt an wie Lesezeichen in Kopf/Fußzeilen exportiert werden.
type: docs
weight: 5050
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

Zeigt an, dass Lesezeichen in Kopf-/Fußzeilen in einem Dokument verarbeitet werden, das wir als PDF rendern.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseOutlines“, um den Gliederungsnavigationsbereich im Ausgabe-PDF anzuzeigen.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Setzen Sie die Eigenschaft „DefaultBookmarksOutlineLevel“ auf „1“, um alle anzuzeigen
// Lesezeichen auf der ersten Ebene der Gliederung im Ausgabe-PDF.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Setzen Sie die Eigenschaft „HeaderFooterBookmarksExportMode“ auf „HeaderFooterBookmarksExportMode.None“.
// keine Lesezeichen exportieren, die sich in Kopf-/Fußzeilen befinden.
// Setzen Sie die Eigenschaft „HeaderFooterBookmarksExportMode“ auf „HeaderFooterBookmarksExportMode.First“.
// Exportiert nur Lesezeichen in der Kopf-/Fußzeile des ersten Abschnitts.
// Setzen Sie die Eigenschaft „HeaderFooterBookmarksExportMode“ auf „HeaderFooterBookmarksExportMode.All“.
// Lesezeichen exportieren, die in allen Kopf-/Fußzeilen enthalten sind.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


