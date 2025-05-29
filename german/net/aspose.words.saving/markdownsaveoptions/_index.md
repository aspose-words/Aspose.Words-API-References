---
title: MarkdownSaveOptions Class
linktitle: MarkdownSaveOptions
articleTitle: MarkdownSaveOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Saving.MarkdownSaveOptions für verbessertes Speichern von Dokumenten im Markdown-Format. Passen Sie Ihre Ausgabe noch heute mit erweiterten Optionen an!
type: docs
weight: 6060
url: /de/net/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class

Klasse zum Festlegen zusätzlicher Optionen beim Speichern eines Dokuments imMarkdown format.

Um mehr zu erfahren, besuchen Sie die[Speicheroptionen festlegen](https://docs.aspose.com/words/net/specify-save-options/) Dokumentationsartikel.

```csharp
public class MarkdownSaveOptions : TxtSaveOptionsBase
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [MarkdownSaveOptions](markdownsaveoptions/)() | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments imMarkdown format. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Konturen beim Einbetten von TrueType-Schriftarten in ein Dokument beim Speichern zulässig ist. Der Standardwert ist`FALSCH` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ruft die benutzerdefinierte lokale Zeitzone ab, die für Datums-/Uhrzeitfelder verwendet wird, oder legt diese fest. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ruft den Pfad zur Standardvorlage ab oder legt ihn fest (einschließlich Dateiname). Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [EmptyParagraphExportMode](../../aspose.words.saving/markdownsaveoptions/emptyparagraphexportmode/) { get; set; } | Gibt an, wie leere Absätze nach Markdown exportiert werden. Der Standardwert istEmptyLine . |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Gibt die Kodierung an, die beim Exportieren in Textformate verwendet werden soll. Der Standardwert ist**Kodierung.UTF8** . |
| [ExportAsHtml](../../aspose.words.saving/markdownsaveoptions/exportashtml/) { get; set; } | Ermöglicht die Angabe der Elemente, die als reines HTML nach Markdown exportiert werden sollen. Der Standardwert istNone . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Wann`WAHR` , bewirkt, dass der Name und die Version von Aspose.Words in die erstellten Dateien eingebettet werden. Der Standardwert ist`WAHR` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Gibt an, wie Kopf- und Fußzeilen in die Textformate exportiert werden. Der Standardwert istPrimaryOnly . |
| [ExportImagesAsBase64](../../aspose.words.saving/markdownsaveoptions/exportimagesasbase64/) { get; set; } | Gibt an, ob Bilder im Base64-Format in der Ausgabedatei gespeichert werden. Der Standardwert ist`FALSCH` . |
| [ExportUnderlineFormatting](../../aspose.words.saving/markdownsaveoptions/exportunderlineformatting/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob die Unterstreichungstextformatierung als Folge von zwei Pluszeichen "++" exportiert werden soll. Der Standardwert ist`FALSCH` . |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Ermöglicht die Angabe, ob die Seitenumbrüche beim Export erhalten bleiben sollen. |
| [ImageResolution](../../aspose.words.saving/markdownsaveoptions/imageresolution/) { get; set; } | Gibt die Ausgabeauflösung für Bilder beim Exportieren nach Markdown an. Standard ist`96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/markdownsaveoptions/imagesavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie Bilder gespeichert werden, wenn ein Dokument in gespeichert wird.Markdown format. |
| [ImagesFolder](../../aspose.words.saving/markdownsaveoptions/imagesfolder/) { get; set; } | Gibt den physischen Ordner an, in dem Bilder gespeichert werden, wenn ein Dokument in exportiert wird.Markdown Format. Standard ist eine leere Zeichenfolge. |
| [ImagesFolderAlias](../../aspose.words.saving/markdownsaveoptions/imagesfolderalias/) { get; set; } | Gibt den Namen des Ordners an, der zum Erstellen der in ein Dokument geschriebenen Bild-URIs verwendet wird. Der Standardwert ist eine leere Zeichenfolge. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie InkML-Objekte gerendert werden. |
| [LinkExportMode](../../aspose.words.saving/markdownsaveoptions/linkexportmode/) { get; set; } | Gibt an, wie Links in die Ausgabedatei geschrieben werden. Der Standardwert istAuto . |
| [ListExportMode](../../aspose.words.saving/markdownsaveoptions/listexportmode/) { get; set; } | Gibt an, wie Listenelemente in die Ausgabedatei geschrieben werden. Der Standardwert istMarkdownSyntax . |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [OfficeMathExportMode](../../aspose.words.saving/markdownsaveoptions/officemathexportmode/) { get; set; } | Gibt an, wie OfficeMath in die Ausgabedatei geschrieben wird. Der Standardwert istText . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Gibt die Zeichenfolge an, die beim Exportieren in Textformate als Absatzumbruch verwendet werden soll. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Wann`WAHR` , formatiert die Ausgabe, wo anwendbar. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten zum Speicherfortschritt. |
| override [SaveFormat](../../aspose.words.saving/markdownsaveoptions/saveformat/) { get; set; } | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nurMarkdown . |
| [TableContentAlignment](../../aspose.words.saving/markdownsaveoptions/tablecontentalignment/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der angibt, wie Inhalte in Tabellen beim Exportieren in dieMarkdown format. Der Standardwert istAuto . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Gibt den Ordner für temporäre Dateien an, der beim Speichern in eine DOC- oder DOCX-Datei verwendet wird. Standardmäßig ist diese Eigenschaft`null` und es werden keine temporären Dateien verwendet. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Bestimmt, ob die Schriftattribute entsprechend dem verwendeten Zeichencode geändert werden. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) Eigenschaft wird vor dem Speichern aktualisiert. Der Standardwert ist`FALSCH` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Anti-Aliasing zum Rendern verwendet werden soll oder nicht. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob qualitativ hochwertige (d. h. langsame) Rendering-Algorithmen verwendet werden sollen oder nicht. |

## Beispiele

Zeigt, wie der Bildname beim Speichern in einem Markdown-Dokument umbenannt wird.

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // Wenn wir ein Dokument, das Bilder enthält, in Markdown konvertieren, erhalten wir am Ende eine Markdown-Datei, die auf mehrere Bilder verweist.
    // Jedes Bild liegt in Form einer Datei im lokalen Dateisystem vor.
    // Es gibt auch einen Rückruf, mit dem der Name und der Dateisystemspeicherort jedes Bildes angepasst werden können.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // Zu diesem Zeitpunkt wird die Methode ImageSaving() unseres Rückrufs ausgeführt.
    doc.Save(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

    Assert.AreEqual(1,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".jpeg")));
    Assert.AreEqual(8,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".png")));
}

/// <summary>
/// Benennt gespeicherte Bilder um, die beim Speichern eines Markdown-Dokuments erstellt werden.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        args.ImageFileName = imageFileName;
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Siehe auch

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
