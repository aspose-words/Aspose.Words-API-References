---
title: TxtLoadOptions Class
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.TxtLoadOptions für verbessertes Laden von Textdokumenten. Passen Sie Ihr Dokumentobjekt mit flexiblen Optionen für optimale Leistung an.
type: docs
weight: 4190
url: /de/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Ermöglicht die Angabe zusätzlicher Optionen beim LadenText Dokument in ein[`Document`](../../aspose.words/document/) Objekt.

Um mehr zu erfahren, besuchen Sie die[Ladeoptionen festlegen](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

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
| [AutoNumberingDetection](../../aspose.words.loading/txtloadoptions/autonumberingdetection/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob beim Laden eines Dokuments eine automatische Nummerierungserkennung durchgeführt wird. Der Standardwert ist`WAHR` . |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um im Dokument gefundene relative URIs bei Bedarf in absolute URIs aufzulösen. Kann sein`null` oder leere Zeichenfolge. Standard ist`null` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ruft ab oder legt fest, ob Metadateien konvertiert werden sollen (Wmf oderEmf ) Bilder zuPngBildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ruft ab oder legt fest, ob Formen mit EquationXML in Office Math-Objekte konvertiert werden sollen. |
| [DetectHyperlinks](../../aspose.words.loading/txtloadoptions/detecthyperlinks/) { get; set; } | Gibt an, ob Hyperlinks im Text erkannt werden sollen. Der Standardwert ist`FALSCH` . |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | Ermöglicht die Angabe, wie nummerierte Listenelemente erkannt werden, wenn das Dokument aus dem Nur-Text-Format importiert wird. Der Standardwert ist`WAHR`. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | Ruft eine Dokumentrichtung ab oder legt sie fest. Der Standardwert istLeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ruft die Kodierung ab oder legt sie fest, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist . Kann sein`null` Standard ist`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Ermöglicht die Festlegung von Schriftarteinstellungen für Dokumente. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Gibt an, ob die OLE-Daten ignoriert werden sollen. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ruft die Spracheinstellungen ab, die beim Laden des Dokuments verwendet werden. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | Ruft die bevorzugte Option für die Behandlung führender Leerzeichen ab oder legt sie fest. Der Standardwert istConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Gibt das Format des zu ladenden Dokuments an. Standard istAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Ermöglicht die Angabe, dass der Dokumentladevorgang einer bestimmten MS Word-Version entsprechen soll. Der Standardwert istWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ruft das Kennwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann`null` oder leere Zeichenfolge. Standard ist`null` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ruft ab oder legt fest, ob das Feld INCLUDEPICTURE beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Wird während des Ladens eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML, MHTML importiert wird. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Ermöglicht die Verwendung temporärer Dateien beim Lesen von Dokumenten. Standardmäßig ist diese Eigenschaft`null` und es werden keine temporären Dateien verwendet. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | Ruft die bevorzugte Option für die Behandlung von Leerzeichen am Ende ab oder legt sie fest. Der Standardwert istTrim . |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Gibt an, ob die Felder mit dem`schmutzig` Attribut. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Ruft ab oder legt fest, ob der aus der Windows-Registrierung abgerufene LCID-Wert zum Bestimmen der Standardränder für die Seiteneinrichtung verwendet werden soll. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungsgenauigkeit führen kann. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |

## Beispiele

Zeigt, wie Hyperlinks gelesen und angezeigt werden.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Dokument mit Hyperlinks laden.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Hyperlinktext drucken.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Siehe auch

* class [LoadOptions](../loadoptions/)
* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
