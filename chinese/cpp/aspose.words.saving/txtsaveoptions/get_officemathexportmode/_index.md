---
title: "Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode 方法"
linktitle: "get_OfficeMathExportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode 方法。指定 OfficeMath 将如何写入输出文件。默认值在 C++ 中为 Text。"
type: docs
weight: 5500
url: /zh/cpp/aspose.words.saving/txtsaveoptions/get_officemathexportmode/
---
## TxtSaveOptions::get_OfficeMathExportMode method


指定 OfficeMath 将如何写入输出文件。默认值为 [Text](../../txtofficemathexportmode/)。

```cpp
Aspose::Words::Saving::TxtOfficeMathExportMode Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode() const
```


## 示例



展示如何在 TXT 中将 OfficeMath 对象导出为 Latex。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## 另见

* Enum [TxtOfficeMathExportMode](../../txtofficemathexportmode/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
