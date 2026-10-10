---
title: "Aspose::Words::Saving::TxtOfficeMathExportMode 枚举"
linktitle: "TxtOfficeMathExportMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::TxtOfficeMathExportMode 枚举。指定 Aspose.Words 在 C++ 中如何将 OfficeMath 导出为文本。"
type: docs
weight: 86250
url: /zh/cpp/aspose.words.saving/txtofficemathexportmode/
---
## TxtOfficeMathExportMode enum


指定 Aspose.Words 如何将 OfficeMath 导出为 [Text](../../aspose.words/saveformat/)。

```cpp
enum class TxtOfficeMathExportMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 文本 | 0 | 将 OfficeMath 导出为纯文本。 |
| Latex | 3 | 将 OfficeMath 导出为 LaTeX。 |


## 示例



展示如何在 TXT 中将 OfficeMath 对象导出为 Latex。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
