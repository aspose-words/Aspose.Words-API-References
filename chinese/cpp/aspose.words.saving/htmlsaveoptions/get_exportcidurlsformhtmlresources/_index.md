---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources 方法"
linktitle: "get_ExportCidUrlsForMhtmlResources"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources 方法。指定是否使用 CID（Content-ID）URL 来引用 MHTML 文档中包含的资源（图像、字体、CSS）。默认值在 C++ 中为 false。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportcidurlsformhtmlresources/
---
## HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method


指定是否使用 CID（Content-ID）URL 来引用 MHTML 文档中包含的资源（图像、字体、CSS）。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources() const
```

## 备注


此选项仅影响保存为 MHTML 的文档。

默认情况下，MHTML 文档中的资源通过文件名引用（例如，"image.png"），这些文件名会与 MIME 部分的 "Content-Location" 头匹配。

此选项启用一种替代方法，将资源文件的引用写为 CID（Content-ID）URL（例如，"cid:image.png"），并与 "Content-ID" 头匹配。

理论上，两种引用方式应该没有区别，任意一种在任何浏览器或邮件客户端都能正常工作。实际上，某些客户端会因文件名而无法获取资源。如果您的浏览器或邮件客户端拒绝加载 MTHML 文档中包含的资源（不显示图像或不加载 CSS 样式），请尝试使用 CID URL 导出文档。

## 示例



展示如何为输出的 MHTML 文档启用内容 ID。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 设置此标志将把 "Content-Location" 标记替换为
// "Content-ID" 标记，针对输入文档中的每个资源。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mhtml);
options->set_ExportCidUrlsForMhtmlResources(exportCidUrlsForMhtmlResources);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-ID: <document.html>"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-Location: document.html"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
