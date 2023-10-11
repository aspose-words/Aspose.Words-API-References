---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Steuert welche Schriftartressourcen beim Speichern in HTML MHTML oder EPUB untergeordnet werden müssen. Die Standardeinstellung ist0 .
type: docs
weight: 290
url: /de/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Steuert, welche Schriftartressourcen beim Speichern in HTML, MHTML oder EPUB untergeordnet werden müssen. Die Standardeinstellung ist`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

### Bemerkungen

[`ExportFontResources`](../exportfontresources/) ermöglicht den Export von Schriftarten als Nebendateien oder als Teile des Pakets „output “. Wenn das Dokument viele Schriftarten verwendet, insbesondere bei einer großen Anzahl von Glyphen, kann die Ausgabegröße erheblich ansteigen. Die Unterteilung von Schriftarten reduziert die Größe der exportierten Schriftartressource, indem Glyphen herausgefiltert werden, die vom aktuellen Dokument nicht verwendet werden.

Die Unterteilung von Schriftarten funktioniert wie folgt:

* Standardmäßig werden alle exportierten Schriftarten in Teilmengen unterteilt.
* Einstellung`FontResourcesSubsettingSizeThreshold`auf einen positiven Wert weist Aspose.Words an, Schriftarten zu unterteilen, deren Dateigröße größer als der angegebene Wert ist.
* Festlegen der Eigenschaft aufMaxValue unterdrückt die Unterteilung von Schriftarten.

**Wichtig!** Beim Exportieren von Schriftartressourcen sollten Aspekte der Schriftartlizenzierung berücksichtigt werden. Autoren, die bestimmte Schriftarten über einen herunterladbaren -Schriftartenmechanismus verwenden möchten, müssen stets sorgfältig prüfen, ob ihre beabsichtigte Verwendung im Rahmen der Schriftartenlizenz liegt. Bei vielen kommerziellen Schriftarten ist das Herunterladen ihrer Schriftarten aus dem Internet in irgendeiner Form derzeit nicht möglich. In Lizenzvereinbarungen, die einige Schriftarten abdecken, wird ausdrücklich darauf hingewiesen, dass die Verwendung durch erfolgt **@Schriftart** Rules in CSS-Stylesheets ist nicht zulässig. Unterteilung von Schriftarten kann ebenfalls gegen Lizenzbedingungen verstoßen.

### Beispiele

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

// Wenn wir das Dokument im HTML-Format speichern, können wir ein SaveOptions-Objekt zum Konfigurieren der Schriftart-Untereinstellung übergeben.
// Angenommen, wir setzen das Flag „ExportFontResources“ auf „true“ und benennen außerdem einen Ordner in der Eigenschaft „FontsFolder“.
// In diesem Fall erstellt der Speichervorgang diesen Ordner und platziert eine .ttf-Datei darin
// dieser Ordner für jede Schriftart, die unser Dokument verwendet.
// Jede .ttf-Datei enthält den gesamten Glyphensatz dieser Schriftart.
// was möglicherweise zu einer sehr großen Datei führen kann, die dem Dokument beiliegt.
// Wenn wir eine Teilmenge auf eine Schriftart anwenden, enthalten die exportierten Rohdaten nur die Glyphen, aus denen das Dokument besteht
// Verwendung anstelle des gesamten Glyphensatzes. Wenn der Text in unserem Dokument nur einen kleinen Bruchteil einer Schriftart verwendet
// Glyphensatz, dann wird die Unterteilung die Größe unserer Ausgabedokumente erheblich reduzieren.
// Wir können die Eigenschaft „FontResourcesSubsettingSizeThreshold“ verwenden, um eine .ttf-Dateigröße in Bytes zu definieren.
 // Wenn eine exportierte Schriftart eine größere Datei erstellt, wendet der Speichervorgang eine Teilmenge auf diese Schriftart an.
// Wenn Sie einen Schwellenwert von 0 festlegen, wird die Teilmenge auf alle Schriftarten angewendet.
// und durch Setzen auf „int.MaxValue“ wird die Teilmenge effektiv deaktiviert.
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
    // Standardmäßig sind die .ttf-Dateien für jede unserer drei Schriftarten über 700 MB groß.
    // Eine Teilmenge reduziert sie alle auf unter 30 MB.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


