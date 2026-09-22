---
title: "Aspose::Words::Node::get_NodeType yöntemi"
linktitle: "get_NodeType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Node::get_NodeType yöntemi. Bu düğümün tipini C++'ta alır."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/node/get_nodetype/
---
## Node::get_NodeType method


Bu düğümün tipini alır.

```cpp
virtual Aspose::Words::NodeType Aspose::Words::Node::get_NodeType() const =0
```


## Örnekler



Bir birleşik düğümden belirli bir türdeki tüm alt düğümleri nasıl kaldıracağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Bu düğümü sildikten sonra ona geçmek isteyebileceğimiz durum için sonraki kardeş düğümü bir değişken olarak kaydet.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // Bir bölüm gövdesi Paragraph ve Table düğümlerini içerebilir.
    // Düğüm bir Tablo ise, onu üst öğeden kaldır.
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```


Bir düğümün NextSibling özelliğini kullanarak doğrudan çocuklarını nasıl yineleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

for (System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_FirstChild(); node != nullptr; node = node->get_NextSibling())
{
    std::cout << std::endl;
    std::cout << System::String::Format(u"Node type: {0}", Aspose::Words::Node::NodeTypeToString(node->get_NodeType())) << std::endl;

    System::String contents = node->GetText().Trim();
    std::cout << (contents == System::String::Empty ? u"This node contains no text" : System::String::Format(u"Contents: \"{0}\"", node->GetText().Trim())) << std::endl;
}
```

## Ayrıca Bakınız

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
