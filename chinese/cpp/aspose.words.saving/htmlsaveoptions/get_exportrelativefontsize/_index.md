---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize 方法"
linktitle: "get_ExportRelativeFontSize"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize 方法。指定在保存为 HTML、MHTML 或 EPUB 时是否应以相对单位输出字体大小。默认在 C++ 中为 false。"
type: docs
weight: 25000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportrelativefontsize/
---
## HtmlSaveOptions::get_ExportRelativeFontSize method


指定在保存为 HTML、MHTML 或 EPUB 时是否以相对单位输出字体大小。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize() const
```

## 备注


在许多现有文档（HTML、IDPF EPUB）中，字体大小是以相对单位指定的。这使得应用程序在查看/处理文档时可以调整文本大小。例如，Microsoft Internet Explorer 有 “View->Text Size” 子菜单，Adobe Digital Editions 有两个按钮：Increase/Decrease Text Size。如果您希望此功能正常工作，则将 [ExportRelativeFontSize](./) 属性设置为 **true**。

**Aspose**[Words](../../../aspose.words/) document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. [Font](../../../aspose.words/font/) size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **%1.5em.** to the HTML.

启用此选项后，除文本之外的文档元素仍将使用绝对尺寸。某些与文本相关的属性也可能以绝对方式表示。特别是，使用 “exactly” 规则指定的行间距在缩放文本时可能产生不希望的结果。因此，在使用 [ExportRelativeFontSize](./) 设置为 **true** 导出时，源文档应进行适当的设计和测试。

## 示例



展示在保存为 .html 时如何使用相对字体大小。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Default font size, ");
builder->get_Font()->set_Size(24);
builder->Writeln(u"2x default font size,");
builder->get_Font()->set_Size(96);
builder->Write(u"8x default font size");

// 当我们将文档保存为 HTML 时，可以传入一个 SaveOptions 对象
// 确定是否使用相对或绝对字体大小。
// 将 "ExportRelativeFontSize" 标志设置为 "true" 以声明字体大小
// 使用 "em" 测量单位，它是一个乘以当前字体大小的因子。
// 将 "ExportRelativeFontSize" 标志设置为 "false" 以声明字体大小
// 使用 "pt" 测量单位，它是字体的绝对点大小。
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

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
