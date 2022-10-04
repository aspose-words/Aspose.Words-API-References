---
title: PdfLoadOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Ermöglicht das Festlegen zusätzlicher Optionen beim Laden eines PDFDokuments in eineDocument../aspose.words/document/ Objekt.
type: docs
weight: 3470
url: /de/net/aspose.words.loading/pdfloadoptions/
---
## PdfLoadOptions class

Ermöglicht das Festlegen zusätzlicher Optionen beim Laden eines PDF-Dokuments in eine[`Document`](../../aspose.words/document/) Objekt.

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
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um im Dokument gefundene relative URIs bei Bedarf in absolute URIs aufzulösen. Kann null oder eine leere Zeichenfolge sein. Standard ist null. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ruft ab oder legt fest, ob Metadatei konvertiert werden soll (Wmf oderEmf ) Bilder zuPng Bildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ruft ab oder legt fest, ob Formen mit EquationXML in Office Math-Objekte konvertiert werden sollen. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ruft die Kodierung ab oder legt sie fest, die verwendet wird, um ein HTML-, TXT- oder CHM-Dokument zu laden, wenn die Kodierung nicht innerhalb des Dokuments angegeben ist. Kann null sein. Standard ist null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Erhält oder setzt einen Wert, der festlegt, welche Dokumentformate abgebildet werden dürfen[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Nur standardmäßigFlatOpc Dokumentformat darf gemappt werden. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Ermöglicht das Festlegen von Schrifteinstellungen für Dokumente. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ruft Spracheinstellungen ab, die beim Laden des Dokuments verwendet werden. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Gibt das Format des zu ladenden Dokuments an. Standard istAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Ermöglicht die Angabe, dass der Dokumentladeprozess mit einer bestimmten MS Word-Version übereinstimmen soll. Der Standardwert istWord2019 |
| [PageCount](../../aspose.words.loading/pdfloadoptions/pagecount/) { get; set; } | Ermittelt oder setzt die Anzahl der zu lesenden Seiten. Standard ist MaxValue, was bedeutet, dass alle Seiten des Dokuments gelesen werden. |
| [PageIndex](../../aspose.words.loading/pdfloadoptions/pageindex/) { get; set; } | Ruft den 0-basierten Index der ersten zu lesenden Seite ab oder legt ihn fest. Standard ist 0. |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ruft das Passwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann null oder eine leere Zeichenfolge sein. Standard ist null. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ruft ab oder legt fest, ob das INCLUDEPICTURE-Feld beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist „false“. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Wird beim Laden eines Dokuments aufgerufen und nimmt Daten zum Ladefortschritt entgegen. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML, MHTML importiert wird. |
| [SkipPdfImages](../../aspose.words.loading/pdfloadoptions/skippdfimages/) { get; set; } | Ruft oder setzt das Flag, das angibt, ob Bilder beim Laden eines PDF-Dokuments übersprungen werden müssen. Standard ist False. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Ermöglicht die Verwendung temporärer Dateien beim Lesen des Dokuments. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Gibt an, ob die Felder mit aktualisiert werden sollen`schmutzig` Attribut. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten oder der Formatierung führen kann. |

### Siehe auch

* class [LoadOptions](../loadoptions/)
* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
