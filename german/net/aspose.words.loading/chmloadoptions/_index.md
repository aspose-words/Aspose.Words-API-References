---
title: ChmLoadOptions Class
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Loading.ChmLoadOptions für verbessertes Laden von CHM-Dokumenten. Passen Sie Ihr Dokumentobjekt mit flexiblen Optionen für optimale Ergebnisse an.
type: docs
weight: 4020
url: /de/net/aspose.words.loading/chmloadoptions/
---
## ChmLoadOptions class

Ermöglicht die Angabe zusätzlicher Optionen beim Laden eines CHM-Dokuments in ein[`Document`](../../aspose.words/document/) Objekt.

Um mehr zu erfahren, besuchen Sie die[Ladeoptionen festlegen](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

```csharp
public class ChmLoadOptions : LoadOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ChmLoadOptions](chmloadoptions/)() | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |

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
| [OriginalFileName](../../aspose.words.loading/chmloadoptions/originalfilename/) { get; set; } | Der Name der CHM-Datei. Der Standardwert ist`null` . |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ruft das Kennwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann`null` oder leere Zeichenfolge. Standard ist`null` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ruft ab oder legt fest, ob das Feld INCLUDEPICTURE beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Wird während des Ladens eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
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

Zeigt, wie URLs wie „ms-its:myfile.chm::/index.htm“ aufgelöst werden.

```csharp
// Unser Dokument enthält URLs wie "ms-its:amhelp.chm::....htm", hat aber einen anderen Namen,
// daher funktionieren Dateilinks nach dem Speichern im HTML-Format nicht.
// Wir müssen den ursprünglichen Dateinamen in „ChmLoadOptions“ definieren, um dieses Verhalten zu vermeiden.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Siehe auch

* class [LoadOptions](../loadoptions/)
* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
