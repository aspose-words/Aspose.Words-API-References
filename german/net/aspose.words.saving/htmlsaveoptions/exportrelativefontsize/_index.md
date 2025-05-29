---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: Aspose.Words für .NET
description: Entdecken Sie die HtmlSaveOptions ExportRelativeFontSize-Eigenschaft, um Schriftgrößen in HTML-, MHTML- oder EPUB-Formaten anzupassen. Verbessern Sie mühelos die Lesbarkeit!
type: docs
weight: 230
url: /de/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

Gibt an, ob Schriftgrößen beim Speichern in HTML, MHTML oder EPUB in relativen Einheiten ausgegeben werden sollen. Standard ist`FALSCH` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

## Bemerkungen

In vielen bestehenden Dokumenten (HTML, IDPF EPUB) werden Schriftgrößen in relativen Einheiten angegeben. Dies ermöglicht es Anwendungen, die Textgröße beim Anzeigen/Bearbeiten von Dokumenten anzupassen. Beispielsweise verfügt Microsoft Internet Explorer über das Untermenü „Ansicht-&gt;Textgröße“, Adobe Digital Editions über zwei Schaltflächen: Textgröße vergrößern/verkleinern. Wenn Sie diese Funktionalität nutzen möchten, setzen Sie`ExportRelativeFontSize` Eigentum zu`WAHR` .

Das Aspose Words-Dokumentmodell verwendet ausschließlich absolute Schriftgrößeneinheiten. Relative Einheiten benötigen zusätzliche Logik, um von einer anfänglichen (Standard-)Größe neu berechnet zu werden. Schriftgröße von**Normal** Als Standard wird der Dokumentstil verwendet. Wenn beispielsweise**Normal** hat 12pt Schriftart und einige Texte sind 18pt, dann wird es output als**1,5 em.** zum HTML.

Wenn diese Option aktiviert ist, haben Dokumentelemente außer Text weiterhin absolute Größen. Auch einige textbezogene Attribute können absolut ausgedrückt werden. Insbesondere kann ein mit der Regel „exakt“ angegebener Zeilenabstand beim Skalieren von Text zu unerwünschten Ergebnissen führen. Daher sollten die Quelldokumente beim Export mit`ExportRelativeFontSize` eingestellt auf`WAHR`.

## Beispiele

Zeigt, wie beim Speichern im HTML-Format relative Schriftgrößen verwendet werden.

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
// Setzen Sie das Flag "ExportRelativeFontSize" auf "true", um Schriftgrößen zu deklarieren
    // unter Verwendung der Maßeinheit „em“, die ein Faktor ist, der die aktuelle Schriftgröße multipliziert.
// Setzen Sie das Flag "ExportRelativeFontSize" auf "false", um Schriftgrößen zu deklarieren
// unter Verwendung der Maßeinheit „pt“, die die absolute Größe der Schriftart in Punkten angibt.
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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
