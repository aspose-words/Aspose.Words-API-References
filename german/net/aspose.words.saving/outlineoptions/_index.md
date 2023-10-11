---
title: Class OutlineOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.OutlineOptions klas. Ermöglicht die Angabe von Umrissoptionen.
type: docs
weight: 5360
url: /de/net/aspose.words.saving/outlineoptions/
---
## OutlineOptions class

Ermöglicht die Angabe von Umrissoptionen.

Um mehr zu erfahren, besuchen Sie die[Speichern Sie ein Dokument](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class OutlineOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [OutlineOptions](outlineoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarksOutlineLevels](../../aspose.words.saving/outlineoptions/bookmarksoutlinelevels/) { get; } | Ermöglicht die Angabe der Gliederungsebene einzelner Lesezeichen. |
| [CreateMissingOutlineLevels](../../aspose.words.saving/outlineoptions/createmissingoutlinelevels/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob fehlende Gliederungsebenen erstellt werden sollen, wenn das Dokument exportiert wird. |
| [CreateOutlinesForHeadingsInTables](../../aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/) { get; set; } | Gibt an, ob Gliederungen für Überschriften (mit den Überschriftenstilen formatierte Absätze) in Tabellen erstellt werden sollen. |
| [DefaultBookmarksOutlineLevel](../../aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/) { get; set; } | Gibt die Standardebene in der Dokumentgliederung an, auf der Word-Lesezeichen angezeigt werden. |
| [ExpandedOutlineLevels](../../aspose.words.saving/outlineoptions/expandedoutlinelevels/) { get; set; } | Gibt an, wie viele Ebenen in der Dokumentgliederung erweitert angezeigt werden sollen, wenn die Datei angezeigt wird. |
| [HeadingsOutlineLevels](../../aspose.words.saving/outlineoptions/headingsoutlinelevels/) { get; set; } | Gibt an, wie viele Überschriftenebenen (mit den Überschriftenstilen formatierte Absätze) in die Dokumentgliederung einbezogen werden sollen. |

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


