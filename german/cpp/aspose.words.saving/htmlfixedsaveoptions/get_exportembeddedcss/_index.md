---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss Methode"
linktitle: "get_ExportEmbeddedCss"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss Methode. Gibt an, ob das CSS (Cascading Style Sheet) in das Html‑Dokument in C++ eingebettet werden soll."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedcss/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedCss method


Gibt an, ob das CSS (Cascading [Stil](../../../aspose.words/style/) Sheet) in das Html‑Dokument eingebettet werden soll.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss() const
```


## Beispiele



Zeigt, wie ermittelt wird, wo CSS‑Stylesheets beim Export eines Dokuments nach Html gespeichert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Wenn wir ein Dokument nach html exportieren, erstellt Aspose.Words ebenfalls ein CSS‑Stylesheet, um das Dokument zu formatieren.
// Durch Setzen des Flags "ExportEmbeddedCss" auf "true" wird das CSS‑Stylesheet in einer .css‑Datei gespeichert,
// und verlinken Sie die Datei aus dem HTML-Dokument mit einem <link>-Element.
// Das Setzen des Flags auf "false" bettet das CSS-Stylesheet in das HTML-Dokument ein,
// was nur eine Datei anstelle von zwei erzeugt.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedCss(exportEmbeddedCss);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<style type=\"text/css\">")->get_Success());
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />")->get_Success());
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

## Siehe auch

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
