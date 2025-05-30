---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre HTML-, MHTML- oder EPUB-Dateien mit der Eigenschaft „FontResourcesSubsettingSizeThreshold“ und sorgen Sie so für eine effiziente Verwaltung der Schriftartressourcen. Standardwert 0.
type: docs
weight: 290
url: /de/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Steuert, welche Schriftartressourcen beim Speichern in HTML, MHTML oder EPUB untergeordnet werden müssen. Standard ist`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Bemerkungen

[`ExportFontResources`](../exportfontresources/) Ermöglicht den Export von Schriftarten als Unterdateien oder als Teil des Ausgabepakets. Wenn das Dokument viele Schriftarten verwendet, insbesondere mit einer großen Anzahl von Glyphen, kann die Ausgabegröße erheblich anwachsen. Die Schriftarten-Subsetierung reduziert die Größe der exportierten Schriftartenressource, indem Glyphen herausgefiltert werden, die im aktuellen Dokument nicht verwendet werden.

Die Schriftart-Untergruppenbildung funktioniert wie folgt:

* Standardmäßig werden alle exportierten Schriftarten in Teilmengen unterteilt.
* Einstellung`FontResourcesSubsettingSizeThreshold` auf einen positiven Wert weist Aspose.Words an, eine Teilmenge der Schriftarten zu erstellen, deren Dateigröße größer als der angegebene Wert ist.
* Festlegen der Eigenschaft aufMaxValue unterdrückt die Unterteilung der Schriftart.

**Wichtig!**Beim Exportieren von Schriftressourcen sollten Sie die Lizenzierung von Schriften berücksichtigen. Autoren, die bestimmte Schriften über einen Download-Mechanismus verwenden möchten, müssen stets sorgfältig prüfen, ob die beabsichtigte Verwendung im Rahmen der Lizenz liegt. Viele kommerzielle Schriften erlauben derzeit keinen Download über das Internet. Lizenzvereinbarungen für bestimmte Schriften weisen ausdrücklich darauf hin, dass die Verwendung über**@Schriftart** Regeln in CSS-Stylesheets sind nicht zulässig. Font-Subsetting kann auch gegen Lizenzbedingungen verstoßen.

## Beispiele

Zeigt, wie mit Schriftart-Untergruppen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// Wenn wir das Dokument im HTML-Format speichern, können wir ein SaveOptions-Objekt übergeben, um die Schriftart-Untergruppe zu konfigurieren.
// Angenommen, wir setzen das Flag „ExportFontResources“ auf „true“ und benennen auch einen Ordner in der Eigenschaft „FontsFolder“.
// In diesem Fall wird beim Speichern dieser Ordner erstellt und eine .ttf-Datei darin abgelegt
// dieser Ordner für jede Schriftart, die unser Dokument verwendet.
// Jede .ttf-Datei enthält den gesamten Glyphensatz dieser Schriftart.
// was möglicherweise zu einer sehr großen Datei führen kann, die dem Dokument beiliegt.
// Wenn wir Subsetting auf eine Schriftart anwenden, enthalten die exportierten Rohdaten nur die Glyphen, die das Dokument
// verwenden anstelle des gesamten Glyphensatzes. Wenn der Text in unserem Dokument nur einen kleinen Teil der Zeichen einer Schriftart verwendet
// Glyphensatz, dann wird durch die Unterteilung die Größe unserer Ausgabedokumente erheblich reduziert.
// Wir können die Eigenschaft „FontResourcesSubsettingSizeThreshold“ verwenden, um eine TTF-Dateigröße in Bytes zu definieren.
    // Wenn eine exportierte Schriftart eine größere Datei erstellt, wird beim Speichern eine Teilmenge auf diese Schriftart angewendet.
// Wenn Sie einen Schwellenwert von 0 festlegen, wird die Teilmenge auf alle Schriftarten angewendet.
// und durch die Einstellung auf „int.MaxValue“ wird die Teilmengenbildung effektiv deaktiviert.
string fontsFolder = ArtifactsDir + "HtmlSaveOptions.FontSubsetting.Fonts";

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontResources = true,
    FontsFolder = fontsFolder,
    FontResourcesSubsettingSizeThreshold = fontResourcesSubsettingSizeThreshold
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FontSubsetting.html", options);

string[] fontFileNames = Directory.GetFiles(fontsFolder).Where(s => s.EndsWith(".ttf")).ToArray();

Assert.AreEqual(3, fontFileNames.Length);

foreach (string filename in fontFileNames)
{
    // Standardmäßig sind die TTF-Dateien für jede unserer drei Schriftarten über 700 MB groß.
    // Durch die Unterteilung werden sie alle auf unter 30 MB reduziert.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
