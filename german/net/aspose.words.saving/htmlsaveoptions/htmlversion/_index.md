---
title: HtmlSaveOptions.HtmlVersion
linktitle: HtmlVersion
articleTitle: HtmlVersion
second_title: Aspose.Words für .NET
description: Entdecken Sie die HtmlSaveOptions HtmlVersion-Eigenschaft, um beim Speichern von Dokumenten im HTML- oder MHTML-Format ganz einfach Ihren HTML-Standard auszuwählen. Optimieren Sie Ihre Ausgabe mühelos!
type: docs
weight: 330
url: /de/net/aspose.words.saving/htmlsaveoptions/htmlversion/
---
## HtmlSaveOptions.HtmlVersion property

Gibt die Version des HTML-Standards an, die beim Speichern des Dokuments im HTML- oder MHTML-Format verwendet werden soll. Der Standardwert istXhtml .

```csharp
public HtmlVersion HtmlVersion { get; set; }
```

## Beispiele

Zeigt, wie eine DOCTYPE-Überschrift angezeigt wird, wenn Dokumente in den Übergangsstandard Xhtml 1.0 konvertiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Unser Dokument enthält nur dann eine DOCTYPE-Deklarationsüberschrift, wenn wir das Flag „ExportXhtmlTransitional“ auf „true“ gesetzt haben.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");
string newLine = Environment.NewLine;

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        $"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{newLine}" +
        $"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{newLine}" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

Zeigt, wie ein Dokument in einer bestimmten HTML-Version gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = htmlVersion,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html", options);

// Unsere HTML-Dokumente weisen geringfügige Unterschiede auf, um mit verschiedenen HTML-Versionen kompatibel zu sein.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case HtmlVersion.Html5:
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<table style=\"padding:0pt; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;
    case HtmlVersion.Xhtml:
        Assert.True(outDocContents.Contains("<a name=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        Assert.True(outDocContents.Contains("<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;
}
```

### Siehe auch

* enum [HtmlVersion](../../htmlversion/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
