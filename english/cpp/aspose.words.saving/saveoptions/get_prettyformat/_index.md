---
title: get_PrettyFormat
second_title: Aspose.Words for C++ API Reference
description: When true, pretty formats output where applicable. Default value is false.
type: docs
weight: 118
url: /cpp/aspose.words.saving/saveoptions/get_prettyformat/
---
## SaveOptions::get_PrettyFormat method


When **true**, pretty formats output where applicable. Default value is **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_PrettyFormat() const
```

## Remarks


Set to **true** to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

## Examples



Shows how to enhance the readability of the raw code of a saved .html document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto htmlOptions = MakeObject<HtmlSaveOptions>(SaveFormat::Html);
htmlOptions->set_PrettyFormat(usePrettyFormat);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// Enabling pretty format makes the raw html code more readable by adding tab stop and new line characters.
String html = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.PrettyFormat.html");

if (usePrettyFormat)
{
    ASSERT_EQ(String(u"<html>\r\n") + u"\t<head>\r\n" + u"\t\t<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />\r\n" +
                  u"\t\t<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />\r\n" +
                  String::Format(u"\t\t<meta name=\"generator\" content=\"{0} {1}\" />\r\n", BuildVersionInfo::get_Product(),
                                 BuildVersionInfo::get_Version()) +
                  u"\t\t<title>\r\n\t\t</title>\r\n" + u"\t</head>\r\n" + u"\t<body style=\"font-family:'Times New Roman'; font-size:12pt\">\r\n" +
                  u"\t\t<div>\r\n" + u"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\r\n" + u"\t\t\t\t<span>Hello world!</span>\r\n" +
                  u"\t\t\t</p>\r\n" + u"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\r\n" +
                  u"\t\t\t\t<span style=\"-aw-import:ignore\">&#xa0;</span>\r\n" + u"\t\t\t</p>\r\n" + u"\t\t</div>\r\n" + u"\t</body>\r\n</html>",
              html);
}
else
{
    ASSERT_EQ(String(u"<html><head><meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />") +
                  u"<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />" +
                  String::Format(u"<meta name=\"generator\" content=\"{0} {1}\" /><title></title></head>", BuildVersionInfo::get_Product(),
                                 BuildVersionInfo::get_Version()) +
                  u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
                  u"<div><p style=\"margin-top:0pt; margin-bottom:0pt\"><span>Hello world!</span></p>" +
                  u"<p style=\"margin-top:0pt; margin-bottom:0pt\"><span style=\"-aw-import:ignore\">&#xa0;</span></p></div></body></html>",
              html);
}
```

## See Also

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
