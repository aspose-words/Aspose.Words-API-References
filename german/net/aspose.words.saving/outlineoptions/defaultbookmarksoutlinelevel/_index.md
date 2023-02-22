---
title: OutlineOptions.DefaultBookmarksOutlineLevel
second_title: Aspose.Words für .NET-API-Referenz
description: OutlineOptions eigendom. Gibt die Standardebene in der Dokumentgliederung an auf der WordLesezeichen angezeigt werden.
type: docs
weight: 50
url: /de/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Gibt die Standardebene in der Dokumentgliederung an, auf der Word-Lesezeichen angezeigt werden.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

### Bemerkungen

Die Ebene einzelner Lesezeichen kann mit angegeben werden[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) Eigentum.

Geben Sie 0 an, und Word-Lesezeichen werden nicht in der Dokumentgliederung angezeigt. Geben Sie 1 an, und Word-Lesezeichen werden in der Dokumentgliederung auf Ebene 1 angezeigt; 2 für Stufe 2 und so weiter.

Der Standardwert ist 0. Der gültige Bereich ist 0 bis 9.

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

* class [OutlineOptions](../)
* namensraum [Aspose.Words.Saving](../../outlineoptions/)
* Montage [Aspose.Words](../../../)


