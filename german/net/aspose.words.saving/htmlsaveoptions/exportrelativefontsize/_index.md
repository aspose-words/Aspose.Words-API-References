---
title: HtmlSaveOptions.ExportRelativeFontSize
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt an ob Schriftgrößen beim Speichern in HTML MHTML oder EPUB in relativen Einheiten ausgegeben werden sollen. Standard istFALSCH .
type: docs
weight: 230
url: /de/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

Gibt an, ob Schriftgrößen beim Speichern in HTML, MHTML oder EPUB in relativen Einheiten ausgegeben werden sollen. Standard ist`FALSCH` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

### Bemerkungen

In vielen vorhandenen Dokumenten (HTML, IDPF EPUB) werden Schriftgrößen in relativen Einheiten angegeben. Dadurch können -Anwendungen die Textgröße beim Anzeigen/Verarbeiten von Dokumenten anpassen. Beispielsweise verfügt Microsoft Internet Explorer über das Untermenü „Ansicht-&gt;Textgröße“, Adobe Digital Editions verfügt über zwei Schaltflächen: Textgröße erhöhen/verringern. Wenn Sie erwarten, dass diese Funktionalität funktioniert, stellen Sie sie ein`ExportRelativeFontSize` Eigentum zu`WAHR` .

Das Aspose Words-Dokumentmodell enthält und arbeitet nur mit absoluten Schriftgrößeneinheiten. Relative Einheiten benötigen zusätzliche Logik, um ausgehend von einer anfänglichen (Standard-)Größe neu berechnet zu werden. Schriftgröße von **Normal** Als Standard wird der Dokumentstil verwendet. Zum Beispiel, wenn **Normal** hat eine Schriftart von 12pt und ein Teil des Textes ist 18pt, dann wird er als ausgegeben **1,5em.** zum HTML.

Wenn diese Option aktiviert ist, haben andere Dokumentelemente als Text weiterhin absolute Größen. Auch einige textbezogene Attribute können absolut ausgedrückt werden. Insbesondere der mit der „exactly“-Regel angegebene Zeilenabstand kann beim Skalieren von Text zu unerwünschten Ergebnissen führen. Daher sollten die Quelldokumente beim Exportieren ordnungsgemäß entworfen und getestet werden`ExportRelativeFontSize` einstellen`WAHR`.

### Beispiele

Zeigt, wie relative Schriftgrößen beim Speichern in .html verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// Wenn wir das Dokument im HTML-Format speichern, können wir ein SaveOptions-Objekt übergeben
// um zu bestimmen, ob relative oder absolute Schriftgrößen verwendet werden sollen.
// Setzen Sie das Flag „ExportRelativeFontSize“ auf „true“, um Schriftgrößen zu deklarieren
 // unter Verwendung der Maßeinheit „em“, einem Faktor, der die aktuelle Schriftgröße multipliziert.
// Setzen Sie das Flag „ExportRelativeFontSize“ auf „false“, um Schriftgrößen zu deklarieren
// unter Verwendung der Maßeinheit „pt“, die der absoluten Größe der Schriftart in Punkt entspricht.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRelativeFontSize = exportRelativeFontSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


