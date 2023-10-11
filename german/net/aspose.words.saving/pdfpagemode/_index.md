---
title: Enum PdfPageMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.PdfPageMode opsomming. Gibt an wie das PDFDokument beim Öffnen im PDFReader angezeigt werden soll.
type: docs
weight: 5500
url: /de/net/aspose.words.saving/pdfpagemode/
---
## PdfPageMode enumeration

Gibt an, wie das PDF-Dokument beim Öffnen im PDF-Reader angezeigt werden soll.

```csharp
public enum PdfPageMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| UseNone | `0` | Weder Dokumentumrisse noch Miniaturbilder sind sichtbar. |
| UseOutlines | `1` | Die Dokumentgliederung ist sichtbar. Beachten Sie, dass der Gliederungsnavigationsbereich ohnehin nicht sichtbar ist, wenn das PDF-Dokument keine Gliederungen enthält. |
| UseThumbs | `2` | Miniaturbilder sind sichtbar. |
| FullScreen | `3` | Vollbildmodus, ohne Menüleiste, Fenstersteuerelemente oder andere sichtbare Fenster. |
| UseOC | `4` | Das optionale Inhaltsgruppenfeld ist sichtbar. |
| UseAttachments | `5` | Das Fenster „Anhänge“ ist sichtbar. |

### Beispiele

Zeigt, wie Anweisungen festgelegt werden, die einige PDF-Reader beim Öffnen eines Ausgabedokuments befolgen sollen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.FullScreen“, damit der PDF-Reader die gespeicherte Datei öffnet
// Dokument im Vollbildmodus, der die Anzeige des Monitors übernimmt und keine sichtbaren Steuerelemente aufweist.
// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseThumbs“, damit der PDF-Reader ein separates Bedienfeld anzeigt
// mit einer Miniaturansicht für jede Seite im Dokument.
// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseOC“, damit der PDF-Reader ein separates Bedienfeld anzeigt
// Damit können wir mit allen im Dokument vorhandenen Ebenen arbeiten.
// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseOutlines“, um den PDF-Reader zu erhalten
// wenn möglich auch um die Gliederung anzuzeigen.
// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseNone“, damit der PDF-Reader nur das Dokument selbst anzeigt.
// Setzen Sie die Eigenschaft „PageMode“ auf „PdfPageMode.UseAttachments“, um das Anhangsfenster sichtbar zu machen.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

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


