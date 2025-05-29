---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „DefaultBookmarksOutlineLevel“ Ihre Word-Dokumente verbessert, indem sie die Sichtbarkeit von Lesezeichen in der Gliederung optimiert. Steigern Sie noch heute Ihre Produktivität!
type: docs
weight: 50
url: /de/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Gibt die Standardebene in der Dokumentgliederung an, auf der Word-Lesezeichen angezeigt werden.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## Bemerkungen

Die einzelnen Lesezeichenebenen können angegeben werden mit[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) Eigentum.

Geben Sie 0 an, und Word-Lesezeichen werden nicht in der Dokumentgliederung angezeigt. Geben Sie 1 an, und Word-Lesezeichen werden in der Dokumentgliederung auf Ebene 1 angezeigt; 2 für Ebene 2 und so weiter.

Der Standardwert ist 0. Gültiger Bereich ist 0 bis 9.

## Beispiele

Zeigt die Verarbeitung von Lesezeichen in Kopf-/Fußzeilen in einem Dokument, das wir in PDF rendern.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseOutlines“, um den Gliederungsnavigationsbereich im Ausgabe-PDF anzuzeigen.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Setzen Sie die Eigenschaft "DefaultBookmarksOutlineLevel" auf "1", um alle
// Lesezeichen auf der ersten Ebene der Gliederung im Ausgabe-PDF.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.None" auf
// keine Lesezeichen exportieren, die sich in Kopf-/Fußzeilen befinden.
// Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.First" auf
// Exportiere nur Lesezeichen in der Kopf-/Fußzeile des ersten Abschnitts.
// Setzen Sie die Eigenschaft "HeaderFooterBookmarksExportMode" auf "HeaderFooterBookmarksExportMode.All" auf
// Lesezeichen exportieren, die in allen Kopf-/Fußzeilen enthalten sind.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Siehe auch

* class [OutlineOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
