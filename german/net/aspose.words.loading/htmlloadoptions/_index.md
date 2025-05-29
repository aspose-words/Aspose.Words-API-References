---
title: HtmlLoadOptions Class
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Loading.HtmlLoadOptions, um das Laden von HTML-Dokumenten in ein Dokumentobjekt mit anpassbaren Optionen für optimale Leistung zu verbessern.
type: docs
weight: 4070
url: /de/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Ermöglicht die Angabe zusätzlicher Optionen beim Laden eines HTML-Dokuments in ein[`Document`](../../aspose.words/document/) Objekt.

Um mehr zu erfahren, besuchen Sie die[Ladeoptionen festlegen](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(*string*) | Eine Verknüpfung zum Initialisieren einer neuen Instanz dieser Klasse mit dem angegebenen Kennwort zum Laden eines verschlüsselten Dokuments. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | Eine Verknüpfung zum Initialisieren einer neuen Instanz dieser Klasse mit Eigenschaften, die auf die angegebenen Werte gesetzt sind. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um im Dokument gefundene relative URIs bei Bedarf in absolute URIs aufzulösen. Kann sein`null` oder leere Zeichenfolge. Standard ist`null` . |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der angibt, wie Eigenschaften von Blockelementen importiert werden. Der Standardwert istMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Ruft ab oder legt fest, ob Metadateien konvertiert werden sollen (Wmf oderEmf ) Bilder zuPngBildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Ruft ab oder legt fest, ob Formen mit EquationXML in Office Math-Objekte konvertiert werden sollen. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der angibt, ob geladene SVG-Bilder in das EMF-Format konvertiert werden sollen. Der Standardwert ist`FALSCH` und geladene SVG-Bilder werden, wenn möglich, unverändert und ohne Konvertierung gespeichert. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Ruft die Kodierung ab oder legt sie fest, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist . Kann sein`null` Standard ist`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Ermöglicht die Festlegung von Schriftarteinstellungen für Dokumente. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob &lt;noscript&gt; HTML-Elemente ignoriert werden sollen. Der Standardwert ist`FALSCH` . |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Gibt an, ob die OLE-Daten ignoriert werden sollen. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Ruft die Spracheinstellungen ab, die beim Laden des Dokuments verwendet werden. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Gibt das Format des zu ladenden Dokuments an. Standard istAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Ermöglicht die Angabe, dass der Dokumentladevorgang einer bestimmten MS Word-Version entsprechen soll. Der Standardwert istWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Ruft das Kennwort zum Öffnen eines verschlüsselten Dokuments ab oder legt es fest. Kann`null` oder leere Zeichenfolge. Standard ist`null` . |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | Ruft den bevorzugten Typ von Dokumentknoten ab oder legt ihn fest, die importierte &lt;input&gt;- und &lt;select&gt;-Elemente darstellen. Der Standardwert istFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Ruft ab oder legt fest, ob das Feld INCLUDEPICTURE beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Wird während des Ladens eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML, MHTML importiert wird. |
| [SupportFontFaceRules](../../aspose.words.loading/htmlloadoptions/supportfontfacerules/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob @font-face-Regeln unterstützt werden und ob deklarierte Schriftarten geladen werden sollen. Der Standardwert ist`FALSCH` . |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob VML-Bilder unterstützt werden sollen. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Ermöglicht die Verwendung temporärer Dateien beim Lesen von Dokumenten. Standardmäßig ist diese Eigenschaft`null` und es werden keine temporären Dateien verwendet. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Gibt an, ob die Felder mit dem`schmutzig` Attribut. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Ruft ab oder legt fest, ob der aus der Windows-Registrierung abgerufene LCID-Wert zum Bestimmen der Standardränder für die Seiteneinrichtung verwendet werden soll. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungsgenauigkeit führen kann. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Die Anzahl der Millisekunden, die gewartet werden soll, bevor die Webanforderung abläuft. Der Standardwert beträgt 100.000 Millisekunden (100 Sekunden). |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |

## Beispiele

Zeigt, wie bedingte Kommentare beim Laden eines HTML-Dokuments unterstützt werden.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Wenn der Wert wahr ist, berücksichtigen wir beim Parsen des geladenen Dokuments den VML-Code.
loadOptions.SupportVml = supportVml;

// Dieses Dokument enthält ein JPEG-Bild innerhalb der Tags "<!--[if gte vml 1]>",
// und ein anderes PNG-Bild innerhalb der Tags "<![if !vml]>".
// Wenn wir das Flag „SupportVml“ auf „true“ setzen, lädt Aspose.Words das JPEG.
// Wenn wir dieses Flag auf „false“ setzen, lädt Aspose.Words nur das PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Siehe auch

* class [LoadOptions](../loadoptions/)
* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
