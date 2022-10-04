---
title: XamlFlowSaveOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Kann verwendet werden um zusätzliche Optionen beim Speichern eines Dokuments im festzulegen.XamlFlow oderXamlFlowPack format.
type: docs
weight: 5420
url: /de/net/aspose.words.saving/xamlflowsaveoptions/
---
## XamlFlowSaveOptions class

Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im festzulegen.XamlFlow oderXamlFlowPack format.

```csharp
public class XamlFlowSaveOptions : SaveOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [XamlFlowSaveOptions](xamlflowsaveoptions/#constructor)() | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannXamlFlow format. |
| [XamlFlowSaveOptions](xamlflowsaveoptions/#constructor_1)(SaveFormat) | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannXamlFlow oderXamlFlowPack format. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Konturen zulässig ist, wenn TrueType-Schriftarten in ein Dokument eingebettet werden, nachdem es gespeichert wurde. Der Standardwert ist **FALSCH** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ruft eine benutzerdefinierte lokale Zeitzone ab oder legt sie fest, die für Datums-/Uhrzeitfelder verwendet wird. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ruft den Pfad zur Standardvorlage (einschließlich Dateiname) ab oder legt ihn fest. Der Standardwert für diese Eigenschaft ist **leerer String** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Wenn wahr, bewirkt dies, dass der Name und die Version von Aspose.Words in produzierte Dateien eingebettet werden. Der Standardwert ist **Stimmt** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Erhält oder setzt einen Wert, der festlegt, welche Dokumentformate abgebildet werden dürfen[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Nur standardmäßigFlatOpc Dokumentformat darf gemappt werden. |
| [ImageSavingCallback](../../aspose.words.saving/xamlflowsaveoptions/imagesavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie Bilder gespeichert werden, wenn ein Dokument in XAML gespeichert wird. |
| [ImagesFolder](../../aspose.words.saving/xamlflowsaveoptions/imagesfolder/) { get; set; } | Gibt den physischen Ordner an, in dem Bilder gespeichert werden, wenn ein Dokument in das XAML-Format exportiert wird. Standard ist eine leere Zeichenfolge. |
| [ImagesFolderAlias](../../aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/) { get; set; } | Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein XAML-Dokument geschrieben werden. Standard ist eine leere Zeichenfolge. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie Ink-Objekte (InkML) gerendert werden. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Holt oder legt einen Wert fest, der bestimmt, ob eine Speicheroptimierung durchgeführt werden soll, bevor das Dokument gespeichert wird. Der Standardwert für diese Eigenschaft ist **FALSCH** . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Wann`Stimmt` , gibt gegebenenfalls hübsche Formate aus. Standardwert ist **FALSCH** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten zum Speicherfortschritt. |
| override [SaveFormat](../../aspose.words.saving/xamlflowsaveoptions/saveformat/) { get; set; } | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nur seinXamlFlow . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Gibt den Ordner für temporäre Dateien an, der beim Speichern in eine DOC- oder DOCX-Datei verwendet wird. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) Eigenschaft wird vor dem Speichern aktualisiert. Standardwert ist false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist **Stimmt** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Erhält oder setzt den Wert, der bestimmt, ob der Inhalt von[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Anti-Aliasing für das Rendern verwendet werden soll oder nicht. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob qualitativ hochwertige (dh langsame) Renderalgorithmen verwendet werden sollen oder nicht. |

### Beispiele

Zeigt, wie die Dateinamen von verknüpften Bildern gedruckt werden, die beim Konvertieren eines Dokuments in Flow-Form-XAML-Dateien erstellt wurden.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Erstellen Sie ein „XamlFlowSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument im XAML-Speicherformat speichern.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Verwenden Sie die Eigenschaft "ImagesFolder", um einen Ordner im lokalen Dateisystem zuzuweisen, in den
    // Aspose.Words speichert alle verknüpften Bilder des Dokuments.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Verwenden Sie die Eigenschaft "ImagesFolderAlias", um diesen Ordner zu verwenden
    // beim Erstellen von Bild-URIs anstelle des Namens des Bildordners.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Ein durch "ImagesFolderAlias" angegebener Ordner muss die Ressourcen anstelle von "ImagesFolder" enthalten.
    // Wir müssen sicherstellen, dass der Ordner existiert, bevor die Streams des Callbacks ihre Ressourcen darin ablegen können.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");

/// <summary>
/// Zählt und druckt Dateinamen von Bildern, während ihr übergeordnetes Dokument in Flow-Form .xaml konvertiert wird.
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // Wenn wir einen Bildordner-Alias angeben, benötigen wir auch
        // Um jeden Stream umzuleiten, um sein Bild in den Alias-Ordner zu legen.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Siehe auch

* class [SaveOptions](../saveoptions/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
