---
title: "Aspose::Words::CompositeNode::GetText yöntemi"
linktitle: "GetText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CompositeNode::GetText yöntemi. C++'da bu düğümün ve tüm alt düğümlerinin metnini alır."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/compositenode/gettext/
---
## CompositeNode::GetText method


Bu düğümün ve tüm alt düğümlerinin metnini alır.

```cpp
System::String Aspose::Words::CompositeNode::GetText() override
```

## Açıklamalar


Dönen dize, [ControlChar](../../controlchar/) içinde açıklandığı gibi tüm kontrol ve özel karakterleri içerir.

## Örnekler



Bir düğümde GetText ve ToString metodlarını çağırma arasındaki farkı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText, görünen metni ve alan kodlarını ayrıca özel karakterleri alacaktır.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015", doc->GetText().Trim());

// ToString, belgeyi belirtilen kaydetme formatına kaydedildiğinde görünümünü verir.
ASSERT_EQ(u"«Field»", doc->ToString(Aspose::Words::SaveFormat::Text).Trim());
```


Bir belgede liste öğesi olan tüm paragrafların nasıl çıktılanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Bulleted list item 1");
builder->Writeln(u"Bulleted list item 2");
builder->Writeln(u"Bulleted list item 3");
builder->get_ListFormat()->RemoveNumbers();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

for (auto&& para : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"This paragraph belongs to list ID# {0}, number style \"{1}\"", para->get_ListFormat()->get_List()->get_ListId(), para->get_ListFormat()->get_ListLevel()->get_NumberStyle()) << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\"", para->GetText().Trim()) << std::endl;
}
```

## Ayrıca Bakınız

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
