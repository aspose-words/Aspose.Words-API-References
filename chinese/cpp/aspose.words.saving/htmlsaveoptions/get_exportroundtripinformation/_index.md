---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation 方法"
linktitle: "get_ExportRoundtripInformation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation 方法。指定在保存为 HTML、MHTML 或 EPUB 时是否写入往返信息。在 C++ 中，HTML 的默认值为 true，MHTML 和 EPUB 的默认值为 false。"
type: docs
weight: 26000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportroundtripinformation/
---
## HtmlSaveOptions::get_ExportRoundtripInformation method


指定在保存为 HTML、MHTML 或 EPUB 时是否写入往返信息。HTML 的默认值为 **true**，而 MHTML 和 EPUB 为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation() const
```

## 备注


[Saving](../../) of the roundtrip information allows to restore document properties such as tab stops, comments, headers and footers during the HTML documents loading back into a [Document](../../../aspose.words/document/) object.

当 **true** 时，往返信息会作为对应 HTML 元素的 -aw-* CSS 属性导出。

当 **false** 时，不会在生成的文件中输出往返信息。

## 示例



展示在转换为 .html 时如何保留隐藏元素。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 在将文档转换为 .html 时，某些元素如隐藏书签、原始形状位置，
// 或脚注将被删除或转换为纯文本，从而实际上丢失。
// 使用 ExportRoundtripInformation 设置为 true 的 HtmlSaveOptions 对象进行保存将保留这些元素。

// 当我们将文档保存为 HTML 时，可以传入 SaveOptions 对象以确定
// 保存操作将如何导出 HTML 不支持或不使用的文档元素，
// 例如隐藏书签和原始形状位置。
// 如果我们将 "ExportRoundtripInformation" 标志设置为 "true"，保存操作将保留这些元素。
// 如果我们将 "ExportRoundTripInformation" 标志设置为 "false"，保存操作将丢弃这些元素。
// 如果我们打算使用 Aspose.Words 加载已保存的 HTML，我们会希望保留此类元素，
// 因为它们可能再次派上用场。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportRoundtripInformation(exportRoundtripInformation);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RoundTripInformation.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.RoundTripInformation.html");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ") + u"padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; -aw-border-bottom:0.5pt single #000000; " + u"-aw-border-left:0.5pt single #000000; -aw-border-right:6pt single #000000; -aw-border-top:0.5pt single #000000\">"));

    ASSERT_TRUE(outDocContents.Contains(u"<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" ") + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span>Page number </span>") + u"<span style=\"-aw-field-start:true\"></span>" + u"<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" + u"<span style=\"-aw-field-separator:true\"></span>" + u"<span>1</span>" + u"<span style=\"-aw-field-end:true\"></span>"));

    ASSERT_EQ(1, doc->get_Range()->get_Fields()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
    {
        return f->get_Type() == Aspose::Words::Fields::FieldType::FieldPage;
    }))));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<div style=\"clear:both\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>&#xa0;</span>"));

    ASSERT_TRUE(outDocContents.Contains(System::String(u"<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ") + u"padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    ASSERT_TRUE(outDocContents.Contains(u"<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    ASSERT_TRUE(outDocContents.Contains(u"<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    ASSERT_TRUE(outDocContents.Contains(u"<span>Page number 1</span>"));

    ASSERT_EQ(0, doc->get_Range()->get_Fields()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
    {
        return f->get_Type() == Aspose::Words::Fields::FieldType::FieldPage;
    }))));
}
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
