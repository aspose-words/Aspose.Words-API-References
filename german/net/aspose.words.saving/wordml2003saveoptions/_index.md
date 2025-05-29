---
title: WordML2003SaveOptions Class
linktitle: WordML2003SaveOptions
articleTitle: WordML2003SaveOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Saving.WordML2003SaveOptions, um Ihr Dokumentspeichererlebnis im WordML-Format mit anpassbaren Optionen zu verbessern.
type: docs
weight: 6480
url: /de/net/aspose.words.saving/wordml2003saveoptions/
---
## WordML2003SaveOptions class

Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments imWordML format.

Um mehr zu erfahren, besuchen Sie die[Speicheroptionen festlegen](https://docs.aspose.com/words/net/specify-save-options/) Dokumentationsartikel.

```csharp
public class WordML2003SaveOptions : SaveOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [WordML2003SaveOptions](wordml2003saveoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Konturen beim Einbetten von TrueType-Schriftarten in ein Dokument beim Speichern zulässig ist. Der Standardwert ist`FALSCH` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ruft die benutzerdefinierte lokale Zeitzone ab, die für Datums-/Uhrzeitfelder verwendet wird, oder legt diese fest. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ruft den Pfad zur Standardvorlage ab oder legt ihn fest (einschließlich Dateiname). Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Wann`WAHR` , bewirkt, dass der Name und die Version von Aspose.Words in die erstellten Dateien eingebettet werden. Der Standardwert ist`WAHR` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie InkML-Objekte gerendert werden. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Wann`WAHR` , formatiert die Ausgabe, wo anwendbar. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten zum Speicherfortschritt. |
| override [SaveFormat](../../aspose.words.saving/wordml2003saveoptions/saveformat/) { get; set; } | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nurWordML . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Gibt den Ordner für temporäre Dateien an, der beim Speichern in eine DOC- oder DOCX-Datei verwendet wird. Standardmäßig ist diese Eigenschaft`null` und es werden keine temporären Dateien verwendet. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Bestimmt, ob die Schriftattribute entsprechend dem verwendeten Zeichencode geändert werden. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) Eigenschaft wird vor dem Speichern aktualisiert. Der Standardwert ist`FALSCH` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Anti-Aliasing zum Rendern verwendet werden soll oder nicht. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob qualitativ hochwertige (d. h. langsame) Rendering-Algorithmen verwendet werden sollen oder nicht. |

## Bemerkungen

Zur Zeit bietet nur die[`SaveFormat`](./saveformat/) Eigenschaft, aber in Zukunft können weitere Optionen hinzugefügt werden.

## Beispiele

Zeigt, wie die Speicheroptimierung verwaltet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie ein "WordML2003SaveOptions"-Objekt, das an die "Save"-Methode des Dokuments übergeben wird
// um die Art und Weise zu ändern, wie wir das Dokument im WordML-Speicherformat speichern.
WordML2003SaveOptions options = new WordML2003SaveOptions();

// Setzen Sie das Flag „MemoryOptimization“ auf „true“, um den Speicherverbrauch zu verringern
// während des Speichervorgangs des Dokuments auf Kosten einer längeren Speicherzeit.
// Setzen Sie das Flag „MemoryOptimization“ auf „false“, um das Dokument normal zu speichern.
options.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.MemoryOptimization.xml", options);
```

Zeigt, wie der Rohinhalt des Ausgabedokuments verwaltet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie ein "WordML2003SaveOptions"-Objekt, das an die "Save"-Methode des Dokuments übergeben wird
// um die Art und Weise zu ändern, wie wir das Dokument im WordML-Speicherformat speichern.
WordML2003SaveOptions options = new WordML2003SaveOptions();

Assert.AreEqual(SaveFormat.WordML, options.SaveFormat);

// Setzen Sie die Eigenschaft "PrettyFormat" auf "true", um die Einrückung von Tabulatorzeichen anzuwenden und
// Zeilenumbrüche, um den Rohinhalt des Ausgabedokuments leichter lesbar zu machen.
// Setzen Sie die Eigenschaft „PrettyFormat“ auf „false“, um den Rohinhalt des Dokuments in einem fortlaufenden Textkörper zu speichern.
options.PrettyFormat = prettyFormat;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml", options);

string fileContents = File.ReadAllText(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml");
string newLine = Environment.NewLine;

if (prettyFormat)
    Assert.True(fileContents.Contains(
        $"<o:DocumentProperties>{newLine}\t\t" +
            $"<o:Revision>1</o:Revision>{newLine}\t\t" +
            $"<o:TotalTime>0</o:TotalTime>{newLine}\t\t" +
            $"<o:Pages>1</o:Pages>{newLine}\t\t" +
            $"<o:Words>0</o:Words>{newLine}\t\t" +
            $"<o:Characters>0</o:Characters>{newLine}\t\t" +
            $"<o:Lines>1</o:Lines>{newLine}\t\t" +
            $"<o:Paragraphs>1</o:Paragraphs>{newLine}\t\t" +
            $"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{newLine}\t\t" +
            $"<o:Version>11.5606</o:Version>{newLine}\t" +
        "</o:DocumentProperties>"));
else
    Assert.True(fileContents.Contains(
        "<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>" +
        "<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
        "<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
```

### Siehe auch

* class [SaveOptions](../saveoptions/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
