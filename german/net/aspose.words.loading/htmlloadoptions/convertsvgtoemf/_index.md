---
title: HtmlLoadOptions.ConvertSvgToEmf
linktitle: ConvertSvgToEmf
articleTitle: ConvertSvgToEmf
second_title: Aspose.Words für .NET
description: HtmlLoadOptions ConvertSvgToEmf eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob geladene SVGBilder in das EMFFormat konvertiert werden sollen. Der Standardwert istFALSCH und wenn möglich werden geladene SVGBilder unverändert ohne Konvertierung gespeichert in C#.
type: docs
weight: 30
url: /de/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob geladene SVG-Bilder in das EMF-Format konvertiert werden sollen. Der Standardwert ist`FALSCH` und wenn möglich werden geladene SVG-Bilder unverändert ohne Konvertierung gespeichert.

```csharp
public bool ConvertSvgToEmf { get; set; }
```

## Bemerkungen

Neuere Versionen von MS Word unterstützen SVG-Bilder nativ. Wenn die in den Ladeoptionen angegebene MS Word-Version SVG unterstützt, speichert Aspose.Words SVG-Bilder unverändert ohne Konvertierung. Wenn SVG nicht unterstützt wird, werden geladene SVG-Bilder in das EMF-Format konvertiert.

Wenn diese Option jedoch auf gesetzt ist`WAHR` , Aspose.Words konvertiert geladene SVG-Bilder in EMF, auch wenn SVG -Bilder von der angegebenen Version von MS Word unterstützt werden.

## Beispiele

Zeigt, wie SVG-Objekte beim Speichern von HTML-Dokumenten in ein anderes Format konvertiert werden.

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// „ConvertSvgToEmf“ verwenden, um das alte Verhalten umzukehren
// wo alle aus einem HTML-Dokument geladenen SVG-Bilder in EMF konvertiert wurden.
// Jetzt werden SVG-Bilder ohne Konvertierung geladen
// wenn die in den Ladeoptionen angegebene MS Word-Version SVG-Bilder nativ unterstützt.
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// Dieses Dokument enthält ein <svg> Element in Form von Text.
// Wenn wir das Dokument im HTML-Format speichern, können wir ein SaveOptions-Objekt übergeben
// um zu bestimmen, wie der Speichervorgang dieses Objekt behandelt.
// Die Eigenschaft „MetafileFormat“ auf „HtmlMetafileFormat.Png“ setzen, um es in ein PNG-Bild zu konvertieren.
// Wenn Sie die Eigenschaft „MetafileFormat“ auf „HtmlMetafileFormat.Svg“ setzen, bleibt es als SVG-Objekt erhalten.
// Die Eigenschaft „MetafileFormat“ auf „HtmlMetafileFormat.EmfOrWmf“ setzen, um sie in eine Metadatei zu konvertieren.
HtmlSaveOptions options = new HtmlSaveOptions { MetafileFormat = htmlMetafileFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case HtmlMetafileFormat.Png:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
    case HtmlMetafileFormat.Svg:
        Assert.True(outDocContents.Contains(
            "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height= \"40\">"));
        break;
    case HtmlMetafileFormat.EmfOrWmf:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
}
```

### Siehe auch

* class [HtmlLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
