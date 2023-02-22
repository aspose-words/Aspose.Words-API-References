---
title: Class OutlineOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.OutlineOptions klas. Ermöglicht das Festlegen von Gliederungsoptionen.
type: docs
weight: 5080
url: /de/net/aspose.words.saving/outlineoptions/
---
## OutlineOptions class

Ermöglicht das Festlegen von Gliederungsoptionen.

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
| [CreateMissingOutlineLevels](../../aspose.words.saving/outlineoptions/createmissingoutlinelevels/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob fehlende Gliederungsebenen erstellt werden, wenn das Dokument exportiert wird. |
| [CreateOutlinesForHeadingsInTables](../../aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/) { get; set; } | Gibt an, ob Gliederungen für Überschriften (Absätze, die mit den Überschriftenstilen formatiert wurden) innerhalb von Tabellen erstellt werden sollen oder nicht. |
| [DefaultBookmarksOutlineLevel](../../aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/) { get; set; } | Gibt die Standardebene in der Dokumentgliederung an, auf der Word-Lesezeichen angezeigt werden. |
| [ExpandedOutlineLevels](../../aspose.words.saving/outlineoptions/expandedoutlinelevels/) { get; set; } | Gibt an, wie viele Ebenen in der Dokumentgliederung erweitert angezeigt werden, wenn die Datei angezeigt wird. |
| [HeadingsOutlineLevels](../../aspose.words.saving/outlineoptions/headingsoutlinelevels/) { get; set; } | Gibt an, wie viele Ebenen von Überschriften (mit den Überschriftenstilen formatierte Absätze) in die -Dokumentgliederung aufgenommen werden sollen. |

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


