---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules 方法"
linktitle: "get_SupportFontFaceRules"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules 方法。获取或设置一个值，指示是否支持 @font-face 规则以及是否加载声明的字体。默认值在 C++ 中为 false。"
type: docs
weight: 6500
url: /zh/cpp/aspose.words.loading/htmlloadoptions/get_supportfontfacerules/
---
## HtmlLoadOptions::get_SupportFontFaceRules method


获取或设置一个值，指示是否支持 @font-face 规则以及是否加载声明的字体。默认值为 **false**。

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules() const
```

## 备注


如果启用此选项，@font-face 规则中声明的字体将被加载并嵌入到生成文档的字体定义中（参见 [FontInfos](../../../aspose.words/documentbase/get_fontinfos/)）。这使得已加载的字体可用于渲染，但在保存时不会自动启用字体嵌入。为了在保存文档时嵌入已加载的字体，应该将 [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) 集合中 [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) 属性设置为 **true**。

支持的字体格式包括 TTF、EOT 和 WOFF。

@font-face 规则在加载 SVG 图像时不受支持。

## 示例



展示如何加载声明的 "@font-face" 规则。
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_SupportFontFaceRules(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Html with FontFace.html", loadOptions);

ASSERT_EQ(u"Squarish Sans CT Regular", doc->get_FontInfos()->idx_get(0)->get_Name());
```

## 另见

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
