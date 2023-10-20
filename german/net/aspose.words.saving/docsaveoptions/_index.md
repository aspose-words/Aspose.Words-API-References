---
title: DocSaveOptions Class
linktitle: DocSaveOptions
articleTitle: DocSaveOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.DocSaveOptions klas. Kann zum Angeben zusätzlicher Optionen beim Speichern eines Dokuments im verwendet werdenDoc or Dot format in C#.
type: docs
weight: 4930
url: /de/net/aspose.words.saving/docsaveoptions/
---
## DocSaveOptions class

Kann zum Angeben zusätzlicher Optionen beim Speichern eines Dokuments im verwendet werdenDoc or Dot format.

Um mehr zu erfahren, besuchen Sie die[Geben Sie Speicheroptionen an](https://docs.aspose.com/words/net/specify-save-options/) Dokumentationsartikel.

```csharp
public class DocSaveOptions : SaveOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [DocSaveOptions](docsaveoptions/#constructor)() | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannDoc format. |
| [DocSaveOptions](docsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannDoc or Dot format. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Umrissen zulässig ist , wenn TrueType-Schriftarten in ein Dokument eingebettet werden, sobald es gespeichert wird. Der Standardwert ist`FALSCH` . |
| [AlwaysCompressMetafiles](../../aspose.words.saving/docsaveoptions/alwayscompressmetafiles/) { get; set; } | Wann`FALSCH` , kleine Metadateien werden aus Leistungsgründen nicht komprimiert. Der Standardwert ist`WAHR` , alle Metadateien werden unabhängig von ihrer Größe komprimiert. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ruft die benutzerdefinierte lokale Zeitzone ab, die für Datums-/Uhrzeitfelder verwendet wird, oder legt diese fest. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ruft den Pfad zur Standardvorlage (einschließlich Dateiname) ab oder legt diesen fest. Der Standardwert für diese Eigenschaft ist**leerer String** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Wann`WAHR` , bewirkt, dass der Name und die Version von Aspose.Words in erzeugte Dateien eingebettet werden. Der Standardwert ist`WAHR` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, wie Ink-Objekte (InkML) gerendert werden. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [Password](../../aspose.words.saving/docsaveoptions/password/) { get; set; } | Ruft ein Passwort ab bzw. legt es fest, um das Dokument mit der RC4-Verschlüsselungsmethode zu verschlüsseln. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Wann`WAHR` hübsche Ausgabeformate, sofern zutreffend. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten über den Speicherfortschritt. |
| override [SaveFormat](../../aspose.words.saving/docsaveoptions/saveformat/) { get; set; } | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann seinDoc oderDot . |
| [SavePictureBullet](../../aspose.words.saving/docsaveoptions/savepicturebullet/) { get; set; } | Wann`FALSCH` , PictureBullet-Daten werden nicht im Ausgabedokument gespeichert. Der Standardwert ist`WAHR` . |
| [SaveRoutingSlip](../../aspose.words.saving/docsaveoptions/saveroutingslip/) { get; set; } | Wann`FALSCH` , RoutingSlip-Daten werden nicht im Ausgabedokument gespeichert. Der Standardwert ist`WAHR` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Gibt den Ordner für temporäre Dateien an, die beim Speichern in einer DOC- oder DOCX-Datei verwendet werden. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) Die Eigenschaft wird vor dem Speichern aktualisiert. Der Standardwert ist`FALSCH` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob Anti-Aliasing für das Rendering verwendet werden soll oder nicht. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob hochwertige (d. h. langsame) Rendering-Algorithmen verwendet werden sollen oder nicht. |

## Bemerkungen

Im Moment bietet nur die[`SaveFormat`](./saveformat/) Eigenschaft, aber in Zukunft werden weitere Optionen hinzugefügt, wie z. B. ein Verschlüsselungskennwort oder Einstellungen für die digitale Signatur.

## Beispiele

Zeigt, wie Speicheroptionen für ältere Microsoft Word-Formate festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Legen Sie ein Passwort fest, das das Laden des Dokuments durch Microsoft Word oder Aspose.Words schützt.
// Beachten Sie, dass dadurch der Inhalt des Dokuments in keiner Weise verschlüsselt wird.
options.Password = "MyPassword";

// Wenn das Dokument einen Laufzettel enthält, können wir ihn beim Speichern beibehalten, indem wir dieses Flag auf true setzen.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Um das Dokument laden zu können,
// Wir müssen das Passwort, das wir im DocSaveOptions-Objekt angegeben haben, in einem LoadOptions-Objekt anwenden.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* class [SaveOptions](../saveoptions/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
