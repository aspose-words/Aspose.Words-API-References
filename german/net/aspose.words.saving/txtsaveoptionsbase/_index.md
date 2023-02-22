---
title: Class TxtSaveOptionsBase
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.TxtSaveOptionsBase klas. Die Basisklasse zum Festlegen zusätzlicher Optionen beim Speichern eines Dokuments in einem textbasierten Format.
type: docs
weight: 5390
url: /de/net/aspose.words.saving/txtsaveoptionsbase/
---
## TxtSaveOptionsBase class

Die Basisklasse zum Festlegen zusätzlicher Optionen beim Speichern eines Dokuments in einem textbasierten Format.

```csharp
public abstract class TxtSaveOptionsBase : SaveOptions
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Konturen zulässig ist, wenn TrueType-Schriftarten in ein Dokument eingebettet werden, nachdem es gespeichert wurde. Der Standardwert ist **FALSCH** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ruft eine benutzerdefinierte lokale Zeitzone ab oder legt sie fest, die für Datums-/Uhrzeitfelder verwendet wird. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ruft den Pfad zur Standardvorlage (einschließlich Dateiname) ab oder legt ihn fest. Der Standardwert für diese Eigenschaft ist **leerer String** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Gibt die beim Export in Textformate zu verwendende Kodierung an. Standardwert ist **Kodierung.UTF8** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Wenn wahr, bewirkt dies, dass der Name und die Version von Aspose.Words in produzierte Dateien eingebettet werden. Der Standardwert ist **Stimmt** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Gibt an, wie Kopf- und Fußzeilen in die Textformate exportiert werden. Standardwert istPrimaryOnly . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Erhält oder setzt einen Wert, der festlegt, welche Dokumentformate abgebildet werden dürfen[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Nur standardmäßigFlatOpc Dokumentformat darf gemappt werden. |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Ermöglicht die Angabe, ob die Seitenumbrüche beim Export beibehalten werden sollen. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie Ink-Objekte (InkML) gerendert werden. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Holt oder legt einen Wert fest, der bestimmt, ob eine Speicheroptimierung durchgeführt werden soll, bevor das Dokument gespeichert wird. Der Standardwert für diese Eigenschaft ist **FALSCH** . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Gibt die Zeichenfolge an, die beim Exportieren in Textformate als Absatzumbruch verwendet werden soll. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Wann`Stimmt` , gibt gegebenenfalls hübsche Formate aus. Standardwert ist **FALSCH** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten zum Speicherfortschritt. |
| abstract [SaveFormat](../../aspose.words.saving/saveoptions/saveformat/) { get; set; } | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Gibt den Ordner für temporäre Dateien an, der beim Speichern in eine DOC- oder DOCX-Datei verwendet wird. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) Eigenschaft wird vor dem Speichern aktualisiert. Standardwert ist false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist **Stimmt** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Erhält oder setzt den Wert, der bestimmt, ob der Inhalt von[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Anti-Aliasing für das Rendern verwendet werden soll oder nicht. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob qualitativ hochwertige (dh langsame) Renderalgorithmen verwendet werden sollen oder nicht. |

### Beispiele

Zeigt, wie ein TXT-Dokument mit einem benutzerdefinierten Absatzumbruch gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument im Klartext speichern.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Setzen Sie "ParagraphBreak" auf einen benutzerdefinierten Wert, den wir am Ende jedes Absatzes einfügen möchten.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Siehe auch

* class [SaveOptions](../saveoptions/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


