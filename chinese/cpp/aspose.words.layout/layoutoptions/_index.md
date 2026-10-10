---
title: "Aspose::Words::Layout::LayoutOptions 类"
linktitle: "LayoutOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutOptions 类。保存允许控制文档布局过程的选项。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.layout/layoutoptions/
---
## LayoutOptions class


保存允许控制文档布局过程的选项。欲了解更多信息，请访问 [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) 文档文章。

```cpp
class LayoutOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Callback](./get_callback/)() const | 获取页面布局模型使用的 [IPageLayoutCallback](../ipagelayoutcallback/) 实现。 |
| [get_CommentDisplayMode](./get_commentdisplaymode/)() const | 获取或设置评论的呈现方式。默认值为 [ShowInBalloons](../commentdisplaymode/)。 |
| [get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/)() const | 获取或设置在连续节重新开始页码时计算页码的行为模式。 |
| [get_IgnorePrinterMetrics](./get_ignoreprintermetrics/)() const | 获取或设置是否忽略 "Use printer metrics to lay out document" 兼容性选项的指示。默认值为 **true**。 |
| [get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/)() const | 获取或设置在字体替换后是否应使用原始字体度量的指示。默认值为 **true**。 |
| [get_RevisionOptions](./get_revisionoptions/)() const | 获取修订选项。 |
| [get_ShowHiddenText](./get_showhiddentext/)() const | 获取或设置指示文档中隐藏文本是否呈现的标志。默认值为 **false**。 |
| [get_ShowParagraphMarks](./get_showparagraphmarks/)() const | 获取或设置指示段落标记是否呈现的标志。默认值为 **false**。 |
| [get_TextShaperFactory](./get_textshaperfactory/)() const | 获取用于高级排版渲染功能的 [ITextShaperFactory](../) 实现。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutOptions](./layoutoptions/)() |  |
| [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::Layout::IPageLayoutCallback\>\&) | 设置页面布局模型使用的 [IPageLayoutCallback](../ipagelayoutcallback/) 实现。 |
| [set_CommentDisplayMode](./set_commentdisplaymode/)(Aspose::Words::Layout::CommentDisplayMode) | 用于设置 [Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode](./get_commentdisplaymode/) 的 setter。 |
| [set_ContinuousSectionPageNumberingRestart](./set_continuoussectionpagenumberingrestart/)(Aspose::Words::Layout::ContinuousSectionRestart) | 用于设置 [Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/) 的 setter。 |
| [set_IgnorePrinterMetrics](./set_ignoreprintermetrics/)(bool) | 用于设置 [Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics](./get_ignoreprintermetrics/) 的 setter。 |
| [set_KeepOriginalFontMetrics](./set_keeporiginalfontmetrics/)(bool) | 用于设置 [Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/) 的 setter。 |
| [set_ShowHiddenText](./set_showhiddentext/)(bool) | 用于设置 [Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText](./get_showhiddentext/) 的 setter。 |
| [set_ShowParagraphMarks](./set_showparagraphmarks/)(bool) | 用于设置 [Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks](./get_showparagraphmarks/) 的 setter。 |
| [set_TextShaperFactory](./set_textshaperfactory/)(const System::SharedPtr\<Aspose::Words::Shaping::ITextShaperFactory\>\&) | 设置用于高级排版渲染功能的 [ITextShaperFactory](../) 实现。 |
| static [Type](./type/)() |  |
## 备注


您不能直接创建此类的实例。请使用 [LayoutOptions](../../aspose.words/document/get_layoutoptions/) 属性来访问此文档的布局选项。

请注意，在更改此类中任何选项后，应调用 [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) 方法，以便将更改的选项应用于布局。

## 示例



展示如何在渲染的输出文档中隐藏文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入隐藏文本，然后指定是否希望在渲染的文档中省略它。
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


展示如何在渲染的输出文档中显示段落标记。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 添加一些段落，然后启用段落标记以显示段落末尾
// 在渲染文档时使用段落符号 (¶)。
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


展示如何更改渲染的输出文档中修订的外观。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入修订，然后将所有修订的颜色更改为绿色。
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// 移除出现在每条修订行左侧的条形标记。
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## 另见

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
