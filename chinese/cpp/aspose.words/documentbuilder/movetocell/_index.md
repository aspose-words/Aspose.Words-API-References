---
title: "Aspose::Words::DocumentBuilder::MoveToCell 方法"
linktitle: "MoveToCell"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::MoveToCell 方法。将光标移动到当前章节中的表格单元格（C++）。"
type: docs
weight: 53000
url: /zh/cpp/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder::MoveToCell method


将光标移动到当前节中的表格单元格。

```cpp
void Aspose::Words::DocumentBuilder::MoveToCell(int32_t tableIndex, int32_t rowIndex, int32_t columnIndex, int32_t characterIndex)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| tableIndex | int32_t | 要移动到的表格索引。 |
| rowIndex | int32_t | 表格中行的索引。 |
| columnIndex | int32_t | 表格中列的索引。 |
| characterIndex | int32_t | 单元格内字符的索引。负值允许您指定从单元格末尾算起的位置。使用 -1 可移动到单元格的末尾。 |
## 备注


导航在当前章节的当前故事中进行。

对于索引参数，当 index 大于或等于 0 时，它表示从开头开始的索引，0 为第一个元素。当 index 小于 0 时，它表示从末尾算起的索引，-1 为最后一个元素。

## 示例



展示如何将 DocumentBuilder 的光标移动到表格中的单元格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个空的 2x2 表格。
builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

// 因为我们已经使用 EndTable 方法结束了表格，
// 文档生成器的光标当前位于表格之外。
// 此光标的功能与 Microsoft Word 的闪烁文本光标相同。
// 它也可以使用生成器的 MoveTo 方法移动到文档中的其他位置。
// 我们可以将光标移回表格内部的特定单元格。
builder->MoveToCell(0, 1, 1, 0);
builder->Write(u"Column 2, cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MoveToCell.docx");
```

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
