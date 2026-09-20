---
title: "Aspose::Words::Fonts::FontInfoCollection class"
linktitle: "FontInfoCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfoCollection class. 表示文档中使用的字体集合。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class


表示文档中使用的字体集合。要了解更多信息，请访问 [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) 文档文章。

```cpp
class FontInfoCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Contains](./contains/)(const System::String\&) | 确定集合是否包含具有给定名称的字体。 |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | 获取集合中包含的元素数量。 |
| [get_EmbedSystemFonts](./get_embedsystemfonts/)() const | 指定是否将系统字体嵌入文档。此属性的默认值为 **false**。仅当 [EmbedTrueTypeFonts](./get_embedtruetypefonts/) 选项设置为 **true** 时，此选项才有效。 |
| [get_EmbedTrueTypeFonts](./get_embedtruetypefonts/)() const | 指定在保存文档时是否嵌入 TrueType 字体。此属性的默认值为 **false**。 |
| [get_SaveSubsetFonts](./get_savesubsetfonts/)() const | 指定是否随文档保存嵌入的 TrueType 字体子集。此属性的默认值为 **false**。仅当 [EmbedTrueTypeFonts](./get_embedtruetypefonts/) 属性设置为 **true** 时，此选项才有效。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个可用于遍历集合中所有项的枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | 获取具有指定名称的字体。 |
| [idx_get](./idx_get/)(int32_t) | 获取指定索引处的字体。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EmbedSystemFonts](./set_embedsystemfonts/)(bool) | 用于 [Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts](./get_embedsystemfonts/) 的设置器。 |
| [set_EmbedTrueTypeFonts](./set_embedtruetypefonts/)(bool) | 用于 [Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts](./get_embedtruetypefonts/) 的设置器。 |
| [set_SaveSubsetFonts](./set_savesubsetfonts/)(bool) | 用于 [Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts](./get_savesubsetfonts/) 的设置器。 |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| 类型定义 | 描述 |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## 备注


项为 [FontInfo](../fontinfo/) 对象。

您不能直接创建此类的实例。请使用 [FontInfos](../../aspose.words/documentbase/get_fontinfos/) 属性来访问文档中定义的字体集合。

## 示例



展示如何打印文档中存在的字体详细信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// 打印文档中所有已使用和未使用的字体。
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


展示如何保存带有嵌入 TrueType 字体的文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## 另见

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
