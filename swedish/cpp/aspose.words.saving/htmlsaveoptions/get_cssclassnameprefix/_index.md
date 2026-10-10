---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix metod"
linktitle: "get_CssClassNamePrefix"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix metod. Anger ett prefix som läggs till alla CSS-klassnamn. Standardvärdet är en tom sträng och genererade CSS-klassnamn har inget gemensamt prefix i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_cssclassnameprefix/
---
## HtmlSaveOptions::get_CssClassNamePrefix method


Anger ett prefix som läggs till alla CSS‑klassnamn. Standardvärdet är en tom sträng och genererade CSS‑klassnamn har inget gemensamt prefix.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix() const
```

## Anmärkningar


Om detta värde inte är tomt, kommer alla CSS-klasser som genereras av Aspose.Words att börja med det angivna prefixet. Detta kan vara användbart, till exempel om du lägger till anpassad CSS till genererade dokument och vill förhindra konflikter med klassnamn.

Om värdet inte är **null** eller tomt, måste det vara en giltig CSS-identifikator.

## Exempel



Visar hur man sparar ett dokument till HTML och lägger till ett prefix till alla dess CSS-klassnamn.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
saveOptions->set_CssClassNamePrefix(u"myprefix-");

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html");

ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Header\">"));
ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Footer\">"));

outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.css");

ASSERT_TRUE(outDocContents.Contains(u".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
ASSERT_TRUE(outDocContents.Contains(u".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
