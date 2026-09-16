---
title: "Aspose::Words::Fonts::FontSettings::SetFontsFolders 方法"
linktitle: "SetFontsFolders"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontSettings::SetFontsFolders 方法。设置 Aspose.Words 在 C++ 中渲染文档或嵌入字体时查找 TrueType 字体的文件夹。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings::SetFontsFolders method


设置 Aspose.Words 在渲染文档或嵌入字体时查找 TrueType 字体的文件夹。

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsFolders(const System::ArrayPtr<System::String> &fontsFolders, bool recursive)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fontsFolders | const System::ArrayPtr\<System::String\>\& | 包含 TrueType 字体的文件夹数组。 |
| recursive | bool | 设为 True 时递归扫描指定文件夹中的字体。 |
## 备注


默认情况下，Aspose.Words 会查找系统中已安装的字体。

设置此属性会重置所有先前加载的字体缓存。

## 示例



展示如何设置多个字体源目录。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// 我们的字体源不包含我们在本文档中用于文本的字体。
// 如果我们在渲染此文档时使用这些字体设置，
// Aspose.Words 将对使用了 Aspose.Words 无法定位的字体的文本应用回退字体。
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());
ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// 默认的字体源缺少我们在此文档中使用的两种字体。
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// 使用 "SetFontsFolders" 方法为我们作为第一个参数传入的每个字体目录创建一个字体源。
// 将 "false" 作为 "recursive" 参数传入，以包含目录中所有字体文件中的字体
// 我们在第一个参数中传入的目录，但不包括这些目录任何子文件夹中的字体。
// 将 "true" 作为 "recursive" 参数传入，以包含我们传入的目录中的所有字体文件
// 在第一个参数中，以及它们子目录中的所有字体。
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsFolders(System::MakeArray<System::String>({get_FontsDir() + u"/Amethysta", get_FontsDir() + u"/Junction"}), recursive);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> newFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(2, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_EQ(1, newFontSources[0]->GetAvailableFonts()->get_Count());
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// "Junction" 文件夹本身不包含字体文件，但其子文件夹中有。
if (recursive)
{
    ASSERT_EQ(11, newFontSources[1]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(newFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Junction Light";
    }))));
}
else
{
    ASSERT_EQ(0, newFontSources[1]->GetAvailableFonts()->get_Count());
}

doc->Save(get_ArtifactsDir() + u"FontSettings.SetFontsFolders.pdf");

// 恢复原始字体源。
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## 另见

* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
