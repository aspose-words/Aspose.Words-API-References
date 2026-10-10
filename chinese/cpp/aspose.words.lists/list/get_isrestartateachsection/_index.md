---
title: "Aspose::Words::Lists::List::get_IsRestartAtEachSection 方法"
linktitle: "get_IsRestartAtEachSection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::List::get_IsRestartAtEachSection 方法。指定列表是否应在每个节重新开始。默认值在 C++ 中为 false。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.lists/list/get_isrestartateachsection/
---
## List::get_IsRestartAtEachSection method


指定列表是否应在每个章节重新开始。默认值为 **false**。

```cpp
bool Aspose::Words::Lists::List::get_IsRestartAtEachSection()
```

## 备注


此选项仅在 RTF、DOC 和 DOCX 文档格式中受支持。

仅当 [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) 高于 [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/) 时，此选项才会写入 DOCX。

## 示例



展示如何配置列表在每个章节重新编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->idx_get(0);
list->set_IsRestartAtEachSection(restartListAtEachSection);

// \"IsRestartAtEachSection\" 属性仅在以下情况下适用
// 文档的 OOXML 合规级别高于 \"OoxmlComplianceCore.Ecma376\" 标准。
auto options = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
options->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

builder->get_ListFormat()->set_List(list);

builder->Writeln(u"List item 1");
builder->Writeln(u"List item 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"List item 3");
builder->Writeln(u"List item 4");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.RestartingDocumentList.docx");

ASPOSE_ASSERT_EQ(restartListAtEachSection, doc->get_Lists()->idx_get(0)->get_IsRestartAtEachSection());
```

## 另见

* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
