---
title: "Aspose::Words::Paragraph::get_ListFormat yöntemi"
linktitle: "get_ListFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Paragraph::get_ListFormat yöntemi. C++'da paragrafın liste biçimlendirme özelliklerine erişim sağlar."
type: docs
weight: 18000
url: /tr/cpp/aspose.words/paragraph/get_listformat/
---
## Paragraph::get_ListFormat method


Paragrafın liste biçimlendirme özelliklerine erişim sağlar.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListFormat> Aspose::Words::Paragraph::get_ListFormat()
```


## Örnekler



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

* Class [ListFormat](../../../aspose.words.lists/listformat/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
