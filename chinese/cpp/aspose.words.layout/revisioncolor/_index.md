---
title: "Aspose::Words::Layout::RevisionColor 枚举"
linktitle: "RevisionColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::RevisionColor 枚举。允许在 C++ 中指定文档修订的颜色。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.layout/revisioncolor/
---
## RevisionColor enum


允许指定文档修订的颜色。

```cpp
enum class RevisionColor
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 自动 | 0 | 默认。 |
| 黑色 | 1 | 表示 000000 颜色。 |
| 蓝色 | 2 | 表示 2e97d3 颜色。 |
| 亮绿色 | 3 | 表示 84a35b 颜色。 |
| 经典蓝色 | 4 | 表示 0000ff 颜色。 |
| 经典红色 | 5 | 表示 ff0000 颜色。 |
| 深蓝色 | 6 | 表示 376e96 颜色。 |
| 深红色 | 7 | 表示 881824 颜色。 |
| 深黄色 | 8 | 表示 e09a2b 颜色。 |
| 灰色25 | 9 | 表示 a0a3a9 颜色。 |
| 灰色50 | 10 | 表示 50565e 颜色。 |
| 绿色 | 11 | 表示 2c6234 颜色。 |
| 粉色 | 12 | 表示 ce338f 颜色。 |
| 红色 | 13 | 表示 b5082e 颜色。 |
| 青色 | 14 | 表示 1b9cab 颜色。 |
| 绿松石色 | 15 | 表示 3eafc2 颜色。 |
| 紫罗兰 | 16 | 表示 633277 颜色。 |
| 白色 | 17 | 表示 ffffff 颜色。 |
| 黄色 | 18 | 表示 fad272 颜色。 |
| 浅粉红 | 19 | 表示 fce6f4 颜色。 |
| 浅蓝色 | 20 | 表示 e1f2fa 颜色。 |
| 浅黄色 | 21 | 表示 fef4de 颜色。 |
| 浅紫色 | 22 | 表示 eadfef 颜色。 |
| 浅橙色 | 23 | 表示 fce3d0 颜色。 |
| 浅绿色 | 24 | 表示 e9f8ce 颜色。 |
| 灰色 | 25 | 表示 efeded 颜色。 |
| 无高亮 | 26 | 未使用颜色来突出显示修订更改。 |
| 按作者 | 27 | 每位作者的修订会从预定义的高对比度颜色集合中获得各自的高亮颜色。 |


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
