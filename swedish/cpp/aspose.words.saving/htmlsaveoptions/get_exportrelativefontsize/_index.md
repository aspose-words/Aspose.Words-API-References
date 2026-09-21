---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize‑metod"
linktitle: "get_ExportRelativeFontSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize‑metod. Anger om teckenstorlekar ska skrivas ut i relativa enheter när man sparar till HTML, MHTML eller EPUB. Standardvärdet är falskt i C++."
type: docs
weight: 25000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportrelativefontsize/
---
## HtmlSaveOptions::get_ExportRelativeFontSize method


Anger om teckenstorlekar ska skrivas ut i relativa enheter när man sparar till HTML, MHTML eller EPUB. Standard är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize() const
```

## Anmärkningar


I många befintliga dokument (HTML, IDPF EPUB) anges teckenstorlekar i relativa enheter. Detta gör det möjligt för applikationer att justera textstorlek vid visning/behandling av dokument. Till exempel har Microsoft Internet Explorer undermenyn "View->Text Size", Adobe Digital Editions har två knappar: Öka/Minska textstorlek. Om du förväntar dig att denna funktionalitet ska fungera, sätt egenskapen [ExportRelativeFontSize](./) till **true**.

**Aspose**[Words](../../../aspose.words/) document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. [Font](../../../aspose.words/font/) size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **%1.5em.** to the HTML.

När detta alternativ är aktiverat kommer dokumentelement som inte är text fortfarande att ha absoluta storlekar. Även vissa textrelaterade attribut kan uttryckas absolut. I synnerhet kan radavstånd som specificerats med regeln "exactly" ge oönskade resultat vid skalning av text. Så bör källdokumenten vara korrekt utformade och testade när de exporteras med [ExportRelativeFontSize](./) satt till **true**.

## Exempel



Visar hur man använder relativa teckenstorlekar vid sparande till .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Default font size, ");
builder->get_Font()->set_Size(24);
builder->Writeln(u"2x default font size,");
builder->get_Font()->set_Size(96);
builder->Write(u"8x default font size");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att avgöra om relativa eller absoluta teckenstorlekar ska användas.
// Ställ in flaggan "ExportRelativeFontSize" till "true" för att ange teckenstorlekar
// med måttenheten "em", som är en faktor som multiplicerar den aktuella teckenstorleken.
// Ställ in flaggan "ExportRelativeFontSize" till "false" för att ange teckenstorlekar
// med måttenheten "pt", som är tecknets absoluta storlek i punkter.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportRelativeFontSize(exportRelativeFontSize);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">") + u"<div>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" + u"<span>2x default font size,</span>" + u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" + u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
