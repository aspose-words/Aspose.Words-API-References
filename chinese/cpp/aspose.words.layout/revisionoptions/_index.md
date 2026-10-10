---
title: "Aspose::Words::Layout::RevisionOptions 类"
linktitle: "RevisionOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::RevisionOptions 类。允许控制文档修订在布局过程中的处理方式。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.layout/revisionoptions/
---
## RevisionOptions class


允许控制布局过程中文档修订的处理方式。欲了解更多信息，请访问 [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) 文档文章。

```cpp
class RevisionOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_CommentColor](./get_commentcolor/)() const | 允许指定用于批注的颜色。默认值是 [Red](../revisioncolor/)。 |
| [get_DeleteCellColor](./get_deletecellcolor/)() | 允许指定用于已删除单元格的颜色 [Deletion](../../aspose.words/revisiontype/)。默认值是 [Pink](../revisioncolor/)。 |
| [get_DeletedTextColor](./get_deletedtextcolor/)() | 允许指定用于已删除内容的颜色 [Deletion](../../aspose.words/revisiontype/)。默认值是 [ByAuthor](../revisioncolor/)。 |
| [get_DeletedTextEffect](./get_deletedtexteffect/)() | 允许指定应用于已删除内容的效果 [Deletion](../../aspose.words/revisiontype/)。默认值是 [StrikeThrough](../revisiontexteffect/) |
| [get_InsertCellColor](./get_insertcellcolor/)() | 允许指定用于已插入单元格的颜色 [Insertion](../../aspose.words/revisiontype/)。默认值是 [Blue](../revisioncolor/)。 |
| [get_InsertedTextColor](./get_insertedtextcolor/)() | 允许指定用于已插入内容的颜色 [Insertion](../../aspose.words/revisiontype/)。默认值是 [ByAuthor](../revisioncolor/)。 |
| [get_InsertedTextEffect](./get_insertedtexteffect/)() | 允许指定应用于已插入内容的效果 [Insertion](../../aspose.words/revisiontype/)。默认值是 [Underline](../revisiontexteffect/)。 |
| [get_MeasurementUnit](./get_measurementunit/)() const | 允许指定修订批注的计量单位。默认值是 [Centimeters](../../aspose.words/measurementunits/) |
| [get_MovedFromTextColor](./get_movedfromtextcolor/)() | 允许指定用于内容移动来源区域的颜色 [Moving](../../aspose.words/revisiontype/)。默认值是 [ByAuthor](../revisioncolor/)。 |
| [get_MovedFromTextEffect](./get_movedfromtexteffect/)() | 允许指定要应用于内容被移动出的区域的效果 [Moving](../../aspose.words/revisiontype/)。默认值是 [DoubleStrikeThrough](../revisiontexteffect/) |
| [get_MovedToTextColor](./get_movedtotextcolor/)() | 允许指定用于内容被移动入的区域的颜色 [Moving](../../aspose.words/revisiontype/)。默认值是 [ByAuthor](../revisioncolor/)。 |
| [get_MovedToTextEffect](./get_movedtotexteffect/)() | 允许指定要应用于内容被移动入的区域的效果 [Moving](../../aspose.words/revisiontype/)。默认值是 [DoubleUnderline](../revisiontexteffect/) |
| [get_RevisedPropertiesColor](./get_revisedpropertiescolor/)() | 允许指定用于具有格式属性更改的内容的颜色 [FormatChange](../../aspose.words/revisiontype/)。默认值是 [NoHighlight](../revisioncolor/)。 |
| [get_RevisedPropertiesEffect](./get_revisedpropertieseffect/)() | 允许指定具有格式属性更改的内容区域的效果 [FormatChange](../../aspose.words/revisiontype/)。默认值是 [None](../revisiontexteffect/)。 |
| [get_RevisionBarsColor](./get_revisionbarscolor/)() const | 允许指定用于标识包含修订信息的文档行的侧栏的颜色。默认值是 [Red](../revisioncolor/)。 |
| [get_RevisionBarsPosition](./get_revisionbarsposition/)() const | 获取或设置修订栏的渲染位置。默认值是 [Outside](../../aspose.words.drawing/horizontalalignment/)。 |
| [get_RevisionBarsWidth](./get_revisionbarswidth/)() const | 获取或设置修订栏的宽度，单位为点。 |
| [get_ShowInBalloons](./get_showinballoons/)() const | 允许指定是否在气泡中渲染修订。默认值是 [None](../showinballoons/)。 |
| [get_ShowOriginalRevision](./get_showoriginalrevision/)() const | 允许指定是否应显示原始文本而不是修订后的文本。默认值是 **false**。 |
| [get_ShowRevisionBars](./get_showrevisionbars/)() const | 允许指定是否应在包含修订内容的行附近渲染修订栏。默认值是 **true**。 |
| [get_ShowRevisionMarks](./get_showrevisionmarks/)() const | 允许指定是否应使用特殊格式标记来标记修订文本。默认值是 **true**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CommentColor](./set_commentcolor/)(Aspose::Words::Layout::RevisionColor) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_CommentColor](./get_commentcolor/) 的 setter。 |
| [set_DeleteCellColor](./set_deletecellcolor/)(Aspose::Words::Layout::RevisionColor) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor](./get_deletecellcolor/) 的 setter。 |
| [set_DeletedTextColor](./set_deletedtextcolor/)(Aspose::Words::Layout::RevisionColor) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_DeletedTextColor](./get_deletedtextcolor/) 的 setter。 |
| [set_DeletedTextEffect](./set_deletedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_DeletedTextEffect](./get_deletedtexteffect/) 的 setter。 |
| [set_InsertCellColor](./set_insertcellcolor/)(Aspose::Words::Layout::RevisionColor) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_InsertCellColor](./get_insertcellcolor/) 的 setter。 |
| [set_InsertedTextColor](./set_insertedtextcolor/)(Aspose::Words::Layout::RevisionColor) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor](./get_insertedtextcolor/) 的 setter。 |
| [set_InsertedTextEffect](./set_insertedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_InsertedTextEffect](./get_insertedtexteffect/) 的 setter。 |
| [set_MeasurementUnit](./set_measurementunit/)(Aspose::Words::MeasurementUnits) | 允许指定修订批注的计量单位。默认值是 [Centimeters](../../aspose.words/measurementunits/) |
| [set_MovedFromTextColor](./set_movedfromtextcolor/)(Aspose::Words::Layout::RevisionColor) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextColor](./get_movedfromtextcolor/) 的 setter。 |
| [set_MovedFromTextEffect](./set_movedfromtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextEffect](./get_movedfromtexteffect/) 的 setter。 |
| [set_MovedToTextColor](./set_movedtotextcolor/)(Aspose::Words::Layout::RevisionColor) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_MovedToTextColor](./get_movedtotextcolor/) 的 setter。 |
| [set_MovedToTextEffect](./set_movedtotexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect](./get_movedtotexteffect/) 的 setter。 |
| [set_RevisedPropertiesColor](./set_revisedpropertiescolor/)(Aspose::Words::Layout::RevisionColor) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor](./get_revisedpropertiescolor/) 的 setter。 |
| [set_RevisedPropertiesEffect](./set_revisedpropertieseffect/)(Aspose::Words::Layout::RevisionTextEffect) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesEffect](./get_revisedpropertieseffect/) 的 setter。 |
| [set_RevisionBarsColor](./set_revisionbarscolor/)(Aspose::Words::Layout::RevisionColor) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor](./get_revisionbarscolor/)。 |
| [set_RevisionBarsPosition](./set_revisionbarsposition/)(Aspose::Words::Drawing::HorizontalAlignment) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition](./get_revisionbarsposition/)。 |
| [set_RevisionBarsWidth](./set_revisionbarswidth/)(float) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsWidth](./get_revisionbarswidth/)。 |
| [set_ShowInBalloons](./set_showinballoons/)(Aspose::Words::Layout::ShowInBalloons) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons](./get_showinballoons/)。 |
| [set_ShowOriginalRevision](./set_showoriginalrevision/)(bool) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision](./get_showoriginalrevision/)。 |
| [set_ShowRevisionBars](./set_showrevisionbars/)(bool) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars](./get_showrevisionbars/)。 |
| [set_ShowRevisionMarks](./set_showrevisionmarks/)(bool) | 用于设置 [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionMarks](./get_showrevisionmarks/)。 |
| static [Type](./type/)() |  |

## 示例



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
