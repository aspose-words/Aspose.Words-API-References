---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins metod"
linktitle: "get_ExportPageMargins"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins‑metod. Anger om sidmarginaler exporteras till HTML, MHTML eller EPUB. Standard är falskt i C++."
type: docs
weight: 23000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagemargins/
---
## HtmlSaveOptions::get_ExportPageMargins method


Anger om sidomarginaler exporteras till HTML, MHTML eller EPUB. Standard är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins() const
```


## Exempel



Visar hur man visar objekt utanför gränserna i utdata‑HTML‑dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Använd en byggare för att infoga en form utan omslag.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 200, 200);

shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Negativa positionsvärden för formen kan placera formen utanför sidans gränser.
// Om vi exporterar detta till HTML kommer formen att visas avkortad.
shape->set_Left(-150);

// När dokumentet sparas till HTML kan vi skicka ett SaveOptions‑objekt
// för att avgöra om sidan ska justeras för att visa objekt utanför gränserna fullt ut.
// Om vi sätter flaggan "ExportPageMargins" till "true" blir formen helt synlig i den exporterade HTML‑en.
// Om vi sätter flaggan "ExportPageMargins" till "false",
// vårt dokument kommer att visa formen avkortad på samma sätt som vi skulle se den i Microsoft Word.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageMargins(exportPageMargins);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    ASSERT_TRUE(outDocContents.Contains(u"<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    ASSERT_TRUE(outDocContents.Contains(u"<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
