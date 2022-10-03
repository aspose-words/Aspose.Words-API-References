---
title: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words für .NET-API-Referenz
description: Steuert welche FontRessourcen beim Speichern in HTML MHTML oder EPUB unterteilt werden müssen. Standard ist0 .
type: docs
weight: 300
url: /de/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Steuert, welche Font-Ressourcen beim Speichern in HTML, MHTML oder EPUB unterteilt werden müssen. Standard ist`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

### Bemerkungen

[`ExportFontResources`](../exportfontresources/) ermöglicht das Exportieren von Schriftarten als untergeordnete Dateien oder als Teile des Pakets output . Wenn das Dokument viele Schriftarten verwendet, insbesondere mit einer großen Anzahl von Glyphen, kann die Ausgabegröße erheblich wachsen. Font-Subsetting reduziert die Größe der exportierten Font-Ressource, indem Glyphen herausgefiltert werden, die nicht vom aktuellen Dokument verwendet werden.

Font-Subsetting funktioniert wie folgt:

* Standardmäßig werden alle exportierten Schriftarten in Untergruppen unterteilt.
* Einstellung`FontResourcesSubsettingSizeThreshold`auf einen positiven Wert weist Aspose.Words an, Schriftarten zu unterteilen, deren Dateigröße größer als der angegebene Wert ist.
* Festlegen der Eigenschaft aufMaxValue unterdrückt Font-Subsetting.

**Wichtig!** Beim Exportieren von Zeichensatzressourcen sollten Probleme mit der Zeichensatzlizenzierung berücksichtigt werden. Autoren, die bestimmte Schriftarten über einen herunterladbaren -Schriftartmechanismus verwenden möchten, müssen immer sorgfältig prüfen, ob ihre beabsichtigte Verwendung im Umfang der Schriftartlizenz liegt. Viele kommerzielle Schriftarten erlauben derzeit nicht das Herunterladen ihrer Schriftarten aus dem Internet in irgendeiner Form. Lizenzvereinbarungen, die einige Schriftarten abdecken, weisen ausdrücklich darauf hin, dass die Verwendung über **@Schriftart** rules in CSS-Stylesheets ist nicht erlaubt. Schriftuntergruppen können auch gegen Lizenzbedingungen verstoßen.

### Beispiele

Zeigt, wie mit Schriftuntergruppen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// Wenn wir das Dokument im HTML-Format speichern, können wir ein SaveOptions-Objekt übergeben, um Schriftuntereinstellungen zu konfigurieren.
// Angenommen, wir setzen das Flag "ExportFontResources" auf "true" und benennen auch einen Ordner in der Eigenschaft "FontsFolder".
// In diesem Fall erstellt der Speichervorgang diesen Ordner und platziert eine .ttf-Datei darin
// dieser Ordner für jede Schriftart, die unser Dokument verwendet.
// Jede .ttf-Datei enthält den gesamten Glyphensatz dieser Schriftart,
// was möglicherweise zu einer sehr großen Datei führen kann, die das Dokument begleitet.
// Wenn wir Subsetting auf einen Font anwenden, enthalten seine exportierten Rohdaten nur die Glyphen, die das Dokument ist
// anstelle des gesamten Glyphensatzes verwenden. Wenn der Text in unserem Dokument nur einen kleinen Bruchteil einer Schriftart verwendet
// Glyph gesetzt, dann wird die Unterteilung die Größe unserer Ausgabedokumente erheblich reduzieren.
// Wir können die Eigenschaft "FontResourcesSubsettingSizeThreshold" verwenden, um eine .ttf-Dateigröße in Bytes zu definieren.
 // Wenn eine exportierte Schriftart eine Datei erstellt, die größer ist als diese, dann wendet der Speichervorgang eine Teileinstellung auf diese Schriftart an.
// Wenn Sie einen Schwellenwert von 0 festlegen, wird die Untergruppe auf alle Schriftarten angewendet.
// und das Setzen auf "int.MaxValue" deaktiviert effektiv die Teilmenge.
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
    // Standardmäßig sind die .ttf-Dateien für jede unserer drei Schriftarten größer als 700 MB.
    // Subsetting reduziert sie alle auf unter 30 MB.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
