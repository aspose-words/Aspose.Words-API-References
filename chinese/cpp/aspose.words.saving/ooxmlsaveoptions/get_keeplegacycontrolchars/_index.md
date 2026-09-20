---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars 方法"
linktitle: "get_KeepLegacyControlChars"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars 方法。保留 C++ 中旧版控制字符的原始表示。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/ooxmlsaveoptions/get_keeplegacycontrolchars/
---
## OoxmlSaveOptions::get_KeepLegacyControlChars method


保留旧版控制字符的原始表示。

```cpp
bool Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars() const
```


## 示例



展示如何在转换为 .docx 时支持旧版控制字符。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// 当我们将文档保存为 OOXML 格式时，可以创建一个 OoxmlSaveOptions 对象
// 然后将其传递给文档的保存方法，以修改文档的保存方式。
// 将 "KeepLegacyControlChars" 属性设置为 "true" 以保留
// 在保存时保留 "ShortDateTime" 旧版字符。
// 将 "KeepLegacyControlChars" 属性设置为 "false" 以移除
// 输出文档中的 "ShortDateTime" 旧版字符。
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## 另见

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
