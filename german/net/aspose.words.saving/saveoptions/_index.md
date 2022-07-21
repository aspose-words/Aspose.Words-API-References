---
title: SaveOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Dies ist eine abstrakte Basisklasse für Klassen die es dem Benutzer ermöglichen zusätzliche -Optionen anzugeben wenn ein Dokument in einem bestimmten Format gespeichert wird.
type: docs
weight: 5300
url: /de/net/aspose.words.saving/saveoptions/
---
## SaveOptions class

Dies ist eine abstrakte Basisklasse für Klassen, die es dem Benutzer ermöglichen, zusätzliche -Optionen anzugeben, wenn ein Dokument in einem bestimmten Format gespeichert wird.

```csharp
public abstract class SaveOptions
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Konturen zulässig ist, wenn TrueType-Schriftarten in ein Dokument eingebettet werden, nachdem es gespeichert wurde. Der Standardwert ist **FALSCH** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Ruft eine benutzerdefinierte lokale Zeitzone ab oder legt sie fest, die für Datums-/Uhrzeitfelder verwendet wird. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Ruft den Pfad zur Standardvorlage (einschließlich Dateiname) ab oder legt ihn fest. Der Standardwert für diese Eigenschaft ist **leerer String** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | Wenn wahr, bewirkt dies, dass der Name und die Version von Aspose.Words in produzierte Dateien eingebettet werden. Der Standardwert ist **Stimmt** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Erhält oder setzt einen Wert, der festlegt, welche Dokumentformate abgebildet werden dürfen[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Nur standardmäßigFlatOpc Dokumentformat darf gemappt werden. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie Ink-Objekte (InkML) gerendert werden. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Holt oder legt einen Wert fest, der bestimmt, ob eine Speicheroptimierung durchgeführt werden soll, bevor das Dokument gespeichert wird. Der Standardwert für diese Eigenschaft ist **FALSCH** . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Wann`Stimmt` , gibt gegebenenfalls hübsche Formate aus. Standardwert ist **FALSCH** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten zum Speicherfortschritt. |
| abstract [SaveFormat](../../aspose.words.saving/saveoptions/saveformat) { get; set; } | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Gibt den Ordner für temporäre Dateien an, der beim Speichern in eine DOC- oder DOCX-Datei verwendet wird. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) Eigenschaft wird vor dem Speichern aktualisiert. Standardwert ist false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist **Stimmt** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Erhält oder setzt den Wert, der bestimmt, ob der Inhalt von[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Anti-Aliasing für das Rendern verwendet werden soll oder nicht. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob qualitativ hochwertige (dh langsame) Renderalgorithmen verwendet werden sollen oder nicht. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [CreateSaveOptions](../../aspose.words.saving/saveoptions/createsaveoptions#createsaveoptions)(SaveFormat) | Erstellt ein Speicheroptionsobjekt einer Klasse, die für das angegebene Speicherformat geeignet ist. |
| static [CreateSaveOptions](../../aspose.words.saving/saveoptions/createsaveoptions#createsaveoptions_1)(string) | Erstellt ein Speicheroptionsobjekt einer Klasse, die für die im angegebenen Dateinamen angegebene Dateierweiterung geeignet ist. |

### Bemerkungen

Eine Instanz der SaveOptions-Klasse oder einer beliebigen abgeleiteten Klasse wird an den Stream übergeben[`Save`](../../aspose.words/document/save) oder Zeichenkette[`Save`](../../aspose.words/document/save) Überladungen für den Benutzer, um benutzerdefinierte Optionen beim Speichern eines Dokuments zu definieren.

### Beispiele

Zeigt, wie Sie beim Speichern eines Dokuments im .epub-Format eine bestimmte Codierung verwenden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Verwenden Sie ein SaveOptions-Objekt, um die Kodierung für ein zu speicherndes Dokument anzugeben.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Standardmäßig hat ein ausgegebenes .epub-Dokument seinen gesamten Inhalt in einem HTML-Teil.
// Ein Split-Kriterium ermöglicht es uns, das Dokument in mehrere HTML-Teile zu segmentieren.
// Wir werden die Kriterien festlegen, um das Dokument in Überschriftenabsätze aufzuteilen.
// Dies ist nützlich für Leser, die keine HTML-Dateien lesen können, die größer als eine bestimmte Größe sind.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Geben Sie an, dass wir Dokumenteigenschaften exportieren möchten.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
