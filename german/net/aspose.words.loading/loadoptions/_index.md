---
title: Class LoadOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Loading.LoadOptions klas. Ermöglicht die Angabe zusätzlicher Optionen z. B. Passwort oder BasisURI wenn ein Dokument in ein geladen wirdDocument Objekt.
type: docs
weight: 3660
url: /de/net/aspose.words.loading/loadoptions/
---
## LoadOptions class

Ermöglicht die Angabe zusätzlicher Optionen (z. B. Passwort oder Basis-URI), wenn ein Dokument in ein geladen wird[`Document`](../../aspose.words/document/) Objekt.

Um mehr zu erfahren, besuchen Sie die[Geben Sie Ladeoptionen an](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

```csharp
public class LoadOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [LoadOptions](loadoptions/#constructor)() | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |
| [LoadOptions](loadoptions/#constructor_2)(string) | Eine Verknüpfung zum Initialisieren einer neuen Instanz dieser Klasse mit dem angegebenen Kennwort, um ein verschlüsseltes Dokument zu laden. |
| [LoadOptions](loadoptions/#constructor_1)(LoadFormat, string, string) | Eine Verknüpfung zum Initialisieren einer neuen Instanz dieser Klasse mit Eigenschaften, die auf die angegebenen Werte festgelegt sind. |

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
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ruft das Passwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann sein`Null` oder leere Zeichenfolge. Standard ist`Null` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ruft ab oder legt fest, ob das INCLUDEPICTURE-Feld beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Wird während des Ladens eines Dokuments aufgerufen und akzeptiert Daten über den Ladefortschritt. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML, MHTML importiert wird. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Ermöglicht die Verwendung temporärer Dateien beim Lesen von Dokumenten. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Gibt an, ob die Felder mit aktualisiert werden sollen`schmutzig` attribute. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungstreue führen könnte. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(object) |  |

### Beispiele

Zeigt, wie ein verschlüsseltes Microsoft Word-Dokument geladen wird.

```csharp
Document doc;

// Aspose.Words löst eine Ausnahme aus, wenn wir versuchen, ein verschlüsseltes Dokument ohne sein Passwort zu öffnen.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Beim Laden eines solchen Dokuments wird das Passwort mithilfe eines LoadOptions-Objekts an den Konstruktor des Dokuments übergeben.
LoadOptions options = new LoadOptions("docPassword");

// Es gibt zwei Möglichkeiten, ein verschlüsseltes Dokument mit einem LoadOptions-Objekt zu laden.
// 1 – Laden Sie das Dokument anhand des Dateinamens aus dem lokalen Dateisystem:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 – Laden Sie das Dokument aus einem Stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Siehe auch

* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)


