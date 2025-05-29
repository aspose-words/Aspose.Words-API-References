---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ExportEmbeddedCss-Eigenschaft von HtmlFixedSaveOptions Ihre HTML-Dokumente durch die Einbettung von CSS für nahtloses Styling verbessert. Optimieren Sie Ihre Webseiten noch heute!
type: docs
weight: 40
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

Gibt an, ob das CSS (Cascading Style Sheet) in das HTML-Dokument eingebettet werden soll.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## Beispiele

Zeigt, wie Sie beim Exportieren eines Dokuments in HTML bestimmen, wo CSS-Stylesheets gespeichert werden sollen.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Wenn wir ein Dokument in HTML exportieren, erstellt Aspose.Words auch ein CSS-Stylesheet, mit dem das Dokument formatiert wird.
// Durch Setzen des Flags „ExportEmbeddedCss“ auf „true“ wird das CSS-Stylesheet in einer CSS-Datei gespeichert.
// und verlinken Sie mit einem <link>-Element vom HTML-Dokument auf die Datei.
// Wenn Sie das Flag auf „false“ setzen, wird das CSS-Stylesheet in das HTML-Dokument eingebettet.
// wodurch nur eine Datei statt zwei erstellt wird.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = exportEmbeddedCss
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    Assert.True(Regex.Match(outDocContents, "<style type=\"text/css\">").Success);
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />").Success);
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
