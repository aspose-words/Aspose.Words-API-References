---
title: Class TxtLoadOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Loading.TxtLoadOptions klas. Ermöglicht die Angabe zusätzlicher Optionen beim LadenText Dokument in einDocument Objekt.
type: docs
weight: 3530
url: /de/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Ermöglicht die Angabe zusätzlicher Optionen beim LadenText Dokument in ein[`Document`](../../aspose.words/document/) Objekt.

```csharp
public class TxtLoadOptions : LoadOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [TxtLoadOptions](txtloadoptions/)() | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um im Dokument gefundene relative URIs bei Bedarf in absolute URIs aufzulösen. Kann null oder eine leere Zeichenfolge sein. Standard ist null. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ruft ab oder legt fest, ob Metadatei konvertiert werden soll (Wmf oderEmf ) Bilder zuPng Bildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ruft ab oder legt fest, ob Formen mit EquationXML in Office Math-Objekte konvertiert werden sollen. |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | Ermöglicht festzulegen, wie nummerierte Listenelemente erkannt werden, wenn ein Dokument aus dem Nur-Text-Format importiert wird. Der Standardwert ist wahr. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | Ruft eine Dokumentrichtung ab oder legt sie fest. Der Standardwert istLeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ruft die Kodierung ab oder legt sie fest, die verwendet wird, um ein HTML-, TXT- oder CHM-Dokument zu laden, wenn die Kodierung nicht innerhalb des Dokuments angegeben ist. Kann null sein. Standard ist null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Erhält oder setzt einen Wert, der festlegt, welche Dokumentformate abgebildet werden dürfen[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Nur standardmäßigFlatOpc Dokumentformat darf gemappt werden. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Ermöglicht das Festlegen von Schrifteinstellungen für Dokumente. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ruft Spracheinstellungen ab, die beim Laden des Dokuments verwendet werden. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | Ermittelt oder setzt die bevorzugte Option einer führenden Leerzeichenbehandlung. Standardwert istConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Gibt das Format des zu ladenden Dokuments an. Standard istAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Ermöglicht die Angabe, dass der Dokumentladeprozess mit einer bestimmten MS Word-Version übereinstimmen soll. Der Standardwert istWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ruft das Passwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann null oder eine leere Zeichenfolge sein. Standard ist null. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ruft ab oder legt fest, ob das INCLUDEPICTURE-Feld beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist „false“. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Wird beim Laden eines Dokuments aufgerufen und nimmt Daten zum Ladefortschritt entgegen. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML, MHTML importiert wird. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Ermöglicht die Verwendung temporärer Dateien beim Lesen des Dokuments. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | Ermittelt oder setzt die bevorzugte Option für die Behandlung von nachgestellten Leerzeichen. Der Standardwert istTrim . |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Gibt an, ob die Felder mit aktualisiert werden sollen`schmutzig` Attribut. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten oder der Formatierung führen kann. |

### Siehe auch

* class [LoadOptions](../loadoptions/)
* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)


