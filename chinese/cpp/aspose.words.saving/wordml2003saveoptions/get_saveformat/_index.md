---
title: "Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat 方法"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat 方法。指定在使用此保存选项对象时文档将保存的格式。仅在 C++ 中只能是 WordML。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.saving/wordml2003saveoptions/get_saveformat/
---
## WordML2003SaveOptions::get_SaveFormat method


指定如果使用此保存选项对象，文档将以何种格式保存。只能是 [WordML](../../../aspose.words/saveformat/)。

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat() override
```


## 示例



展示如何管理输出文档的原始内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// 创建一个 "WordML2003SaveOptions" 对象，以传递给文档的 "Save" 方法
// 以修改我们将文档保存为 WordML 格式的方式。
auto options = System::MakeObject<Aspose::Words::Saving::WordML2003SaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::WordML, options->get_SaveFormat());

// 将 "PrettyFormat" 属性设置为 "true" 以应用制表符缩进和
// 换行，使输出文档的原始内容更易阅读。
// 将 "PrettyFormat" 属性设置为 "false"，以将文档的原始内容保存为连续的文本体。
options->set_PrettyFormat(prettyFormat);

doc->Save(get_ArtifactsDir() + u"WordML2003SaveOptions.PrettyFormat.xml", options);

System::String fileContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"WordML2003SaveOptions.PrettyFormat.xml");
System::String newLine = System::Environment::get_NewLine();
if (prettyFormat)
{
    ASSERT_TRUE(fileContents.Contains(System::String::Format(u"<o:DocumentProperties>{0}\t\t", newLine) + System::String::Format(u"<o:Revision>1</o:Revision>{0}\t\t", newLine) + System::String::Format(u"<o:TotalTime>0</o:TotalTime>{0}\t\t", newLine) + System::String::Format(u"<o:Pages>1</o:Pages>{0}\t\t", newLine) + System::String::Format(u"<o:Words>0</o:Words>{0}\t\t", newLine) + System::String::Format(u"<o:Characters>0</o:Characters>{0}\t\t", newLine) + System::String::Format(u"<o:Lines>1</o:Lines>{0}\t\t", newLine) + System::String::Format(u"<o:Paragraphs>1</o:Paragraphs>{0}\t\t", newLine) + System::String::Format(u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{0}\t\t", newLine) + System::String::Format(u"<o:Version>11.5606</o:Version>{0}\t", newLine) + u"</o:DocumentProperties>"));
}
else
{
    ASSERT_TRUE(fileContents.Contains(System::String(u"<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>") + u"<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" + u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
}
```

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [WordML2003SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
