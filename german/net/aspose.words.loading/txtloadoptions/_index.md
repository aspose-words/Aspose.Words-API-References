---
title: Class TxtLoadOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Loading.TxtLoadOptions klas. Ermöglicht die Angabe zusätzlicher Optionen beim LadenText Dokument in einDocument Objekt.
type: docs
weight: 3730
url: /de/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Ermöglicht die Angabe zusätzlicher Optionen beim LadenText Dokument in ein[`Document`](../../aspose.words/document/) Objekt.

Um mehr zu erfahren, besuchen Sie die[Geben Sie Ladeoptionen an](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

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
| [AutoNumberingDetection](../../aspose.words.loading/txtloadoptions/autonumberingdetection/) { get; set; } | Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob beim Laden eines Dokuments eine automatische Nummerierungserkennung durchgeführt wird. Der Standardwert ist`WAHR` . |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ruft die Zeichenfolge ab oder legt diese fest, die bei Bedarf zum Auflösen relativer URIs im Dokument in absolute URIs verwendet wird. Kann sein`Null` oder leere Zeichenfolge. Standard ist`Null` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ruft ab oder legt fest, ob die Metadatei konvertiert werden soll (Wmf oderEmf ) Bilder zuPng Bildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ruft ab oder legt fest, ob Formen mit EquationXML in Office Math-Objekte konvertiert werden sollen. |
| [DetectHyperlinks](../../aspose.words.loading/txtloadoptions/detecthyperlinks/) { get; set; } |  |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | Ermöglicht die Angabe, wie nummerierte Listenelemente erkannt werden, wenn ein Dokument aus dem Nur-Text-Format importiert wird. Der Standardwert ist`WAHR`. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | Ruft eine Dokumentrichtung ab oder legt sie fest. Der Standardwert istLeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ruft die Kodierung ab, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, oder legt diese fest, wenn die Kodierung im Dokument nicht angegeben ist . Kann sein`Null` . Standard ist`Null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Ermöglicht das Festlegen von Schriftarteinstellungen für Dokumente. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Gibt an, ob die OLE-Daten ignoriert werden sollen. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ruft Spracheinstellungen ab, die beim Laden des Dokuments verwendet werden. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | Ruft die bevorzugte Option einer führenden Leerzeichenbehandlung ab oder legt diese fest. Der Standardwert istConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Gibt das Format des zu ladenden Dokuments an. Standard istAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Ermöglicht die Angabe, dass der Dokumentladevorgang mit einer bestimmten MS Word-Version übereinstimmen soll. Der Standardwert istWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ruft das Passwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann sein`Null` oder leere Zeichenfolge. Standard ist`Null` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ruft ab oder legt fest, ob das INCLUDEPICTURE-Feld beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Wird während des Ladens eines Dokuments aufgerufen und akzeptiert Daten über den Ladefortschritt. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML, MHTML importiert wird. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Ermöglicht die Verwendung temporärer Dateien beim Lesen von Dokumenten. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | Ruft die bevorzugte Option einer nachgestellten Leerzeichenbehandlung ab oder legt diese fest. Der Standardwert istTrim . |
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


