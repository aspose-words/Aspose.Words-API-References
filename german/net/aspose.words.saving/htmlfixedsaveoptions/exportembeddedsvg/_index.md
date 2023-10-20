---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: Aspose.Words für .NET
description: HtmlFixedSaveOptions ExportEmbeddedSvg eigendom. Gibt an ob SVGRessourcen in ein HTMLDokument eingebettet werden sollen. Der Standardwert istWAHR  in C#.
type: docs
weight: 70
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

Gibt an, ob SVG-Ressourcen in ein HTML-Dokument eingebettet werden sollen. Der Standardwert ist`WAHR` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## Beispiele

Zeigt, wie Sie bestimmen, wo SVG-Objekte gespeichert werden sollen, wenn Sie ein Dokument in HTML exportieren.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Wenn wir ein Dokument mit SVG-Objekten nach .html exportieren,
// Aspose.Words kann diese Objekte an zwei möglichen Orten platzieren.
// Wenn Sie das Flag „ExportEmbeddedSvg“ auf „true“ setzen, werden alle SVG-Objekt-Rohdaten eingebettet
// innerhalb des Ausgabe-HTML, innerhalb von <image> Stichworte.
// Wenn Sie dieses Flag auf „false“ setzen, wird für jedes SVG-Objekt eine Datei im lokalen Dateisystem erstellt.
// Der HTML-Code wird über das „data“-Attribut eines <object> mit jeder Datei verknüpft. Etikett.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedSvg = exportSvgs
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<image id=\"image004\" xlink:href=.+/>").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>").Success);
}
```

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
