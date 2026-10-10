---
title: "Aspose::Words::DocumentBase::get_Styles 方法"
linktitle: "get_Styles"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBase::get_Styles 方法。返回 C++ 中文档中定义的样式集合。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/documentbase/get_styles/
---
## DocumentBase::get_Styles method


返回文档中定义的样式集合。

```cpp
System::SharedPtr<Aspose::Words::StyleCollection> Aspose::Words::DocumentBase::get_Styles() const
```

## 备注


欲了解更多信息，请参阅 [StyleCollection](../../stylecollection/) 类的描述。

## 示例



展示如何访问文档的样式集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// 枚举并列出使用 Aspose.Words 创建的文档默认包含的所有样式。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> stylesEnum = doc->get_Styles()->GetEnumerator();
    while (stylesEnum->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Style> curStyle = stylesEnum->get_Current();
        std::cout << System::String::Format(u"Style name:\t\"{0}\", of type \"{1}\"", curStyle->get_Name(), curStyle->get_Type()) << std::endl;
        std::cout << System::String::Format(u"\tSubsequent style:\t{0}", curStyle->get_NextParagraphStyleName()) << std::endl;
        std::cout << System::String::Format(u"\tIs heading:\t\t\t{0}", curStyle->get_IsHeading()) << std::endl;
        std::cout << System::String::Format(u"\tIs QuickStyle:\t\t{0}", curStyle->get_IsQuickStyle()) << std::endl;

        ASPOSE_ASSERT_EQ(doc, curStyle->get_Document());
    }
}
```


展示如何创建并使用带列表格式的段落样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建自定义段落样式。
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// 创建列表，并确保使用此样式的段落将使用该列表。
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// 将段落样式应用于文档生成器的当前段落，然后添加一些文本。
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// 将文档生成器的样式更改为没有列表格式的样式，并写入另一段落。
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## 另见

* Class [StyleCollection](../../stylecollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
