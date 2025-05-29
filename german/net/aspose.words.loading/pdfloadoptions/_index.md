---
title: PdfLoadOptions Class
linktitle: PdfLoadOptions
articleTitle: PdfLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.PdfLoadOptions für verbessertes Laden von PDF-Dateien. Passen Sie Ihre Dokumentkonvertierungen mit flexiblen Optionen für optimale Ergebnisse an.
type: docs
weight: 4130
url: /de/net/aspose.words.loading/pdfloadoptions/
---
## PdfLoadOptions class

Ermöglicht die Angabe zusätzlicher Optionen beim Laden eines PDF-Dokuments in ein[`Document`](../../aspose.words/document/) Objekt.

Um mehr zu erfahren, besuchen Sie die[Ladeoptionen festlegen](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

```csharp
public class PdfLoadOptions : LoadOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PdfLoadOptions](pdfloadoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um im Dokument gefundene relative URIs bei Bedarf in absolute URIs aufzulösen. Kann sein`null` oder leere Zeichenfolge. Standard ist`null` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ruft ab oder legt fest, ob Metadateien konvertiert werden sollen (Wmf oderEmf ) Bilder zuPngBildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ruft ab oder legt fest, ob Formen mit EquationXML in Office Math-Objekte konvertiert werden sollen. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ruft die Kodierung ab oder legt sie fest, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist . Kann sein`null` Standard ist`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Ermöglicht die Festlegung von Schriftarteinstellungen für Dokumente. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Gibt an, ob die OLE-Daten ignoriert werden sollen. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ruft die Spracheinstellungen ab, die beim Laden des Dokuments verwendet werden. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Gibt das Format des zu ladenden Dokuments an. Standard istAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Ermöglicht die Angabe, dass der Dokumentladevorgang einer bestimmten MS Word-Version entsprechen soll. Der Standardwert istWord2019 |
| [PageCount](../../aspose.words.loading/pdfloadoptions/pagecount/) { get; set; } | Ruft die Anzahl der zu lesenden Seiten ab oder legt sie fest. Der Standardwert ist MaxValue, d. h., es werden alle Seiten des Dokuments gelesen. |
| [PageIndex](../../aspose.words.loading/pdfloadoptions/pageindex/) { get; set; } | Ruft den 0-basierten Index der ersten zu lesenden Seite ab oder legt ihn fest. Der Standardwert ist 0. |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ruft das Kennwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann`null` oder leere Zeichenfolge. Standard ist`null` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ruft ab oder legt fest, ob das Feld INCLUDEPICTURE beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Wird während des Ladens eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML, MHTML importiert wird. |
| [SkipPdfImages](../../aspose.words.loading/pdfloadoptions/skippdfimages/) { get; set; } | Ruft das Flag ab oder setzt es, das angibt, ob Bilder beim Laden eines PDF-Dokuments übersprungen werden sollen. Der Standardwert ist`FALSCH` . |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Ermöglicht die Verwendung temporärer Dateien beim Lesen von Dokumenten. Standardmäßig ist diese Eigenschaft`null` und es werden keine temporären Dateien verwendet. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Gibt an, ob die Felder mit dem`schmutzig` Attribut. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Ruft ab oder legt fest, ob der aus der Windows-Registrierung abgerufene LCID-Wert zum Bestimmen der Standardränder für die Seiteneinrichtung verwendet werden soll. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungsgenauigkeit führen kann. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |

## Beispiele

Zeigt, wie Bilder beim Laden von PDF-Dateien übersprungen werden.

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;
options.PageIndex = 0;
options.PageCount = 1;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
    Assert.AreEqual(shapeCollection.Count, 0);
else
    Assert.AreNotEqual(shapeCollection.Count, 0);
```

### Siehe auch

* class [LoadOptions](../loadoptions/)
* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
