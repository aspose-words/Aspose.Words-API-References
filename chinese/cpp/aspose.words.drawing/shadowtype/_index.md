---
title: "Aspose::Words::Drawing::ShadowType enum"
linktitle: "ShadowType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShadowType enum. 指定 C++ 中形状阴影的类型。"
type: docs
weight: 35000
url: /zh/cpp/aspose.words.drawing/shadowtype/
---
## ShadowType enum


指定形状阴影的类型。

```cpp
enum class ShadowType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| ShadowMixed | -2 | 没有预定义的阴影预设。 |
| Shadow1 | 1 | 第一种阴影类型。 |
| Shadow10 | 10 | 第十种阴影类型。 |
| Shadow11 | 11 | 第十一种阴影类型。 |
| Shadow12 | 12 | 第十二种阴影类型。 |
| Shadow13 | 13 | 第十三种阴影类型。 |
| Shadow14 | 14 | 第十四种阴影类型。 |
| Shadow15 | 15 | 第十五种阴影类型。 |
| Shadow16 | 16 | 第十六种阴影类型。 |
| Shadow17 | 17 | 第十七种阴影类型。 |
| Shadow18 | 18 | 第十八种阴影类型。 |
| Shadow19 | 19 | 第十九种阴影类型。 |
| Shadow2 | 2 | 第二种阴影类型。 |
| Shadow20 | 20 | 第二十种阴影类型。 |
| Shadow21 | 21 | 第二十一种阴影类型。 |
| Shadow22 | 22 | 第二十二种阴影类型。 |
| Shadow23 | 23 | 第二十三种阴影类型。 |
| Shadow24 | 24 | 第二十四种阴影类型。 |
| Shadow25 | 25 | 第二十五种阴影类型。 |
| Shadow26 | 26 | 第二十六种阴影类型。 |
| Shadow27 | 27 | 第二十七种阴影类型。 |
| Shadow28 | 28 | 第二十八种阴影类型。 |
| Shadow29 | 29 | 第二十九种阴影类型。 |
| Shadow3 | 3 | 第三种阴影类型。 |
| Shadow30 | 30 | 第三十种阴影类型。 |
| Shadow31 | 31 | 第三十一种阴影类型。 |
| Shadow32 | 32 | 第三十二种阴影类型。 |
| Shadow33 | 33 | 第三十三种阴影类型。 |
| Shadow34 | 34 | 第三十四种阴影类型。 |
| Shadow35 | 35 | 第三十五种阴影类型。 |
| Shadow36 | 36 | 第三十六种阴影类型。 |
| Shadow37 | 37 | 第三十七种阴影类型。 |
| Shadow38 | 38 | 第三十八种阴影类型。 |
| Shadow39 | 39 | 第三十九种阴影类型。 |
| Shadow4 | 4 | 第四种阴影类型。 |
| Shadow40 | 40 | 第四十种阴影类型。 |
| Shadow41 | 41 | 第四十一种阴影类型。 |
| Shadow42 | 42 | 第四十二种阴影类型。 |
| Shadow43 | 43 | 第四十三种阴影类型。 |
| Shadow5 | 5 | 第五种阴影类型。 |
| Shadow6 | 6 | 第六种阴影类型。 |
| Shadow7 | 7 | 第七种阴影类型。 |
| Shadow8 | 8 | 第八种阴影类型。 |
| Shadow9 | 9 | 第九种阴影类型。 |


## 示例



展示如何对形状使用阴影格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

if (shape->get_ShadowFormat()->get_Visible() && shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::Shadow2)
{
    shape->get_ShadowFormat()->set_Type(Aspose::Words::Drawing::ShadowType::Shadow7);
}

if (shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::ShadowMixed)
{
    shape->get_ShadowFormat()->Clear();
}
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
