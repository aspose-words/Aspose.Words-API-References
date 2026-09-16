---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter method"
linktitle: "get_IgnoreHeaderFooter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter 方法。获取或设置一个布尔值，用于指定在使用 KeepSourceFormatting 模式时是否忽略标题/页脚内容的源格式。默认值在 C++ 中为 true。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/importformatoptions/get_ignoreheaderfooter/
---
## ImportFormatOptions::get_IgnoreHeaderFooter method


获取或设置一个布尔值，用于指定在使用 [KeepSourceFormatting](../../importformatmode/) 模式时是否忽略标题/页脚内容的源格式。默认值为 **true**。

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter() const
```


## 示例



展示如何指定是否忽略标题/页脚内容的源格式。
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// 如果 'IgnoreHeaderFooter' 为 false，则使用标题/页脚内容的原始格式
// 来自 "Header and footer types.docx" 的内容将被使用。
// 如果 'IgnoreHeaderFooter' 为 true，则标题/页脚内容的格式
// 来自 "Document.docx" 的内容将被使用。
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreHeaderFooter(false);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

## 另见

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
