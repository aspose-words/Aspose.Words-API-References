---
title: RtfLoadOptions Class
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.RtfLoadOptions, um das Laden von RTF-Dokumenten mit anpassbaren Einstellungen für eine nahtlose Integration in Ihre Projekte zu verbessern.
type: docs
weight: 4170
url: /de/net/aspose.words.loading/rtfloadoptions/
---
## RtfLoadOptions class

Ermöglicht die Angabe zusätzlicher Optionen beim LadenRtf Dokument in ein[`Document`](../../aspose.words/document/) Objekt.

Um mehr zu erfahren, besuchen Sie die[Ladeoptionen festlegen](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

```csharp
public class RtfLoadOptions : LoadOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [RtfLoadOptions](rtfloadoptions/)() | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |

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
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ruft das Kennwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann`null` oder leere Zeichenfolge. Standard ist`null` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ruft ab oder legt fest, ob das Feld INCLUDEPICTURE beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Wird während des Ladens eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [RecognizeUtf8Text](../../aspose.words.loading/rtfloadoptions/recognizeutf8text/) { get; set; } | Bei Einstellung auf`WAHR` , versucht, UTF8-Zeichen zu erkennen, sie bleiben beim Import erhalten. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML, MHTML importiert wird. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Ermöglicht die Verwendung temporärer Dateien beim Lesen von Dokumenten. Standardmäßig ist diese Eigenschaft`null` und es werden keine temporären Dateien verwendet. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Gibt an, ob die Felder mit dem`schmutzig` Attribut. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Ruft ab oder legt fest, ob der aus der Windows-Registrierung abgerufene LCID-Wert zum Bestimmen der Standardränder für die Seiteneinrichtung verwendet werden soll. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungsgenauigkeit führen kann. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |

## Beispiele

Zeigt, wie beim Laden eines RTF-Dokuments UTF-8-Zeichen erkannt werden.

```csharp
// Erstellen Sie ein „RtfLoadOptions“-Objekt, um zu ändern, wie wir ein RTF-Dokument laden.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Setzen Sie die Eigenschaft „RecognizeUtf8Text“ auf „false“, um anzunehmen, dass das Dokument den Zeichensatz ISO 8859-1 verwendet
// und lädt jedes Zeichen im Dokument.
// Setzen Sie die Eigenschaft „RecognizeUtf8Text“ auf „true“, um alle im Text vorkommenden Zeichen variabler Länge zu analysieren.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### Siehe auch

* class [LoadOptions](../loadoptions/)
* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
