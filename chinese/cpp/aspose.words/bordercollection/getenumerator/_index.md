---
title: "Aspose::Words::BorderCollection::GetEnumerator 方法"
linktitle: "GetEnumerator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BorderCollection::GetEnumerator 方法。返回一个可用于在 C++ 中遍历集合中所有边框的枚举器对象。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words/bordercollection/getenumerator/
---
## BorderCollection::GetEnumerator method


返回一个可用于遍历集合中所有边框的枚举器对象。

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> Aspose::Words::BorderCollection::GetEnumerator() override
```


## 示例



展示如何遍历并编辑段落格式对象中的所有边框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 配置构建器的段落格式设置，以在所有侧面创建绿色波浪边框。
System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> enumerator = borders->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Border> border = enumerator->get_Current();
        border->set_Color(System::Drawing::Color::get_Green());
        border->set_LineStyle(Aspose::Words::LineStyle::Wave);
        border->set_LineWidth(3);
    }
}

// 插入一个段落。我们的边框设置将决定其边框的外观。
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"BorderCollection.GetBordersEnumerator.docx");
```

## 另见

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
