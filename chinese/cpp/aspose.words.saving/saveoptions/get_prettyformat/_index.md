---
title: "Aspose::Words::Saving::SaveOptions::get_PrettyFormat 方法"
linktitle: "get_PrettyFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_PrettyFormat 方法。当为 true 时，对适用的输出进行美化格式化。默认值在 C++ 中为 false。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.saving/saveoptions/get_prettyformat/
---
## SaveOptions::get_PrettyFormat method


当 **true** 时，在适用的情况下对输出进行美化格式化。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::SaveOptions::get_PrettyFormat() const
```

## 备注


设置为 **true** 可使 HTML、MHTML、EPUB、WordML、RTF、DOCX 和 ODT 输出可读性更高。对测试或调试很有帮助。

## 示例



展示如何提升已保存 .html 文档的原始代码可读性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto htmlOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
htmlOptions->set_PrettyFormat(usePrettyFormat);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// 启用美化格式会通过添加制表符和换行符，使原始 html 代码更易读。
System::String html = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.PrettyFormat.html");

System::String newLine = System::Environment::get_NewLine();
if (usePrettyFormat)
{
    ASSERT_EQ(System::String::Format(u"<html>{0}", newLine) + System::String::Format(u"\t<head>{0}", newLine) + System::String::Format(u"\t\t<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />{0}", newLine) + System::String::Format(u"\t\t<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />{0}", newLine) + System::String::Format(u"\t\t<meta name=\"generator\" content=\"{0} {1}\" />{2}", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version(), newLine) + System::String::Format(u"\t\t<title>{0}", newLine) + System::String::Format(u"\t\t</title>{0}", newLine) + System::String::Format(u"\t</head>{0}", newLine) + System::String::Format(u"\t<body style=\"font-family:'Times New Roman'; font-size:12pt\">{0}", newLine) + System::String::Format(u"\t\t<div>{0}", newLine) + System::String::Format(u"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">{0}", newLine) + System::String::Format(u"\t\t\t\t<span>Hello world!</span>{0}", newLine) + System::String::Format(u"\t\t\t</p>{0}", newLine) + System::String::Format(u"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">{0}", newLine) + System::String::Format(u"\t\t\t\t<span style=\"-aw-import:ignore\">&#xa0;</span>{0}", newLine) + System::String::Format(u"\t\t\t</p>{0}", newLine) + System::String::Format(u"\t\t</div>{0}", newLine) + System::String::Format(u"\t</body>{0}</html>", newLine), html);
}
else
{
    ASSERT_EQ(System::String(u"<html><head><meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />") + u"<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />" + System::String::Format(u"<meta name=\"generator\" content=\"{0} {1}\" /><title></title></head>", Aspose::Words::BuildVersionInfo::get_Product(), Aspose::Words::BuildVersionInfo::get_Version()) + u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">" + u"<div><p style=\"margin-top:0pt; margin-bottom:0pt\"><span>Hello world!</span></p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt\"><span style=\"-aw-import:ignore\">&#xa0;</span></p></div></body></html>", html);
}
```

## 另见

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
