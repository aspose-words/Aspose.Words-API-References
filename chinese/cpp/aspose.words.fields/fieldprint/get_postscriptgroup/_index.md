---
title: "Aspose::Words::Fields::FieldPrint::get_PostScriptGroup 方法"
linktitle: "get_PostScriptGroup"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldPrint::get_PostScriptGroup 方法。在 C++ 中获取或设置 PostScript 指令操作的绘图矩形。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldprint/get_postscriptgroup/
---
## FieldPrint::get_PostScriptGroup method


获取或设置 PostScript 指令操作的绘图矩形。

```cpp
System::String Aspose::Words::Fields::FieldPrint::get_PostScriptGroup()
```


## 示例



显示如何插入 PRINT 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"My paragraph");

// PRINT 字段可以向打印机发送指令。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrint>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPrint, true));

// 设置打印机执行指令的区域。
// 在这种情况下，它将是包含我们 PRINT 字段的段落。
field->set_PostScriptGroup(u"para");

// 当我们使用支持 PostScript 的打印机来打印文档时，
// 此命令将把我们在 "field.PostScriptGroup" 中指定的整个区域变为白色。
field->set_PrinterInstructions(u"erasepage");

ASSERT_EQ(u" PRINT  erasepage \\p para", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.PRINT.docx");
```

## 另见

* Class [FieldPrint](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
