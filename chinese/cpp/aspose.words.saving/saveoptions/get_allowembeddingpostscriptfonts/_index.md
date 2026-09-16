---
title: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts 方法"
linktitle: "get_AllowEmbeddingPostScriptFonts"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts 方法。获取或设置一个布尔值，指示在保存文档时嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体。默认值在 C++ 中为 false。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/saveoptions/get_allowembeddingpostscriptfonts/
---
## SaveOptions::get_AllowEmbeddingPostScriptFonts method


获取或设置一个布尔值，指示在文档保存时是否允许在嵌入 TrueType 字体时嵌入带有 PostScript 描边的字体。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts() const
```

## 备注


注意，Word 不会嵌入 PostScript 字体，但可以打开嵌入此类字体的文档。

此选项仅在 [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) 的 [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) 属性设置为 **true** 时生效。

## 示例



展示如何使用 PostScript 字体保存文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"PostScriptFont");
builder->Writeln(u"Some text with PostScript font.");

// 加载带有 PostScript 的字体以在文档中使用。
auto otf = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(System::IO::File::ReadAllBytes(get_FontsDir() + u"AllegroOpen.otf"));
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({otf}));

// 嵌入 TrueType 字体。
doc->get_FontInfos()->set_EmbedTrueTypeFonts(true);

// 在嵌入 TrueType 字体时允许嵌入 PostScript 字体。
// Microsoft Word 不会嵌入 PostScript 字体，但可以打开嵌入此类字体的文档。
System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat::Docx);
saveOptions->set_AllowEmbeddingPostScriptFonts(true);

doc->Save(get_ArtifactsDir() + u"Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

## 另见

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
