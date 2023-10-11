---
title: Class PdfLoadOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Loading.PdfLoadOptions klas. Ermöglicht die Angabe zusätzlicher Optionen beim Laden eines PDFDokuments in einDocument Objekt.
type: docs
weight: 3670
url: /de/net/aspose.words.loading/pdfloadoptions/
---
## PdfLoadOptions class

Ermöglicht die Angabe zusätzlicher Optionen beim Laden eines PDF-Dokuments in ein[`Document`](../../aspose.words/document/) Objekt.

Um mehr zu erfahren, besuchen Sie die[Geben Sie Ladeoptionen an](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

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
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ruft die Zeichenfolge ab oder legt diese fest, die bei Bedarf zum Auflösen relativer URIs im Dokument in absolute URIs verwendet wird. Kann sein`Null` oder leere Zeichenfolge. Standard ist`Null` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ruft ab oder legt fest, ob die Metadatei konvertiert werden soll (Wmf oderEmf ) Bilder zuPng Bildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ruft ab oder legt fest, ob Formen mit EquationXML in Office Math-Objekte konvertiert werden sollen. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ruft die Kodierung ab, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, oder legt diese fest, wenn die Kodierung im Dokument nicht angegeben ist . Kann sein`Null` . Standard ist`Null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Ermöglicht das Festlegen von Schriftarteinstellungen für Dokumente. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Gibt an, ob die OLE-Daten ignoriert werden sollen. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ruft Spracheinstellungen ab, die beim Laden des Dokuments verwendet werden. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Gibt das Format des zu ladenden Dokuments an. Standard istAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Ermöglicht die Angabe, dass der Dokumentladevorgang mit einer bestimmten MS Word-Version übereinstimmen soll. Der Standardwert istWord2019 |
| [PageCount](../../aspose.words.loading/pdfloadoptions/pagecount/) { get; set; } | Ruft die Anzahl der zu lesenden Seiten ab oder legt diese fest. Der Standardwert ist MaxValue, was bedeutet, dass alle Seiten des Dokuments gelesen werden. |
| [PageIndex](../../aspose.words.loading/pdfloadoptions/pageindex/) { get; set; } | Ruft den 0-basierten Index der ersten zu lesenden Seite ab oder legt diesen fest. Der Standardwert ist 0. |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ruft das Passwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann sein`Null` oder leere Zeichenfolge. Standard ist`Null` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ruft ab oder legt fest, ob das INCLUDEPICTURE-Feld beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Wird während des Ladens eines Dokuments aufgerufen und akzeptiert Daten über den Ladefortschritt. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML, MHTML importiert wird. |
| [SkipPdfImages](../../aspose.words.loading/pdfloadoptions/skippdfimages/) { get; set; } | Ruft das Flag ab oder setzt es, das angibt, ob Bilder beim Laden eines PDF-Dokuments übersprungen werden müssen. Standard ist`FALSCH` . |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Ermöglicht die Verwendung temporärer Dateien beim Lesen von Dokumenten. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Gibt an, ob die Felder mit aktualisiert werden sollen`schmutzig` attribute. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungstreue führen könnte. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(object) |  |

### Siehe auch

* class [LoadOptions](../loadoptions/)
* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)


