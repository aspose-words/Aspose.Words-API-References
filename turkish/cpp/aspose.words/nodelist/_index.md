---
title: "Aspose::Words::NodeList class"
linktitle: "NodeList"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeList class. XPath sorgusuyla eşleşen düğümlerin, SelectNodes() yöntemi kullanılarak yürütülen bir koleksiyonunu temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 45000
url: /tr/cpp/aspose.words/nodelist/
---
## NodeList class


XPath sorgusuyla eşleşen düğümlerin bir koleksiyonunu temsil eder ve [SelectNodes()](../) yöntemi kullanılarak yürütülür. Daha fazla bilgi edinmek için, [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokümantasyon makalesini ziyaret edin.

```cpp
class NodeList : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Count](./get_count/)() const | Listedeki düğüm sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Düğümlerin koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) const | Verilen indeksteki bir düğümü alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeList](./nodelist/)(const System::SharedPtr\<Aspose::Words::NodeCollection\>\&) |  |
| [ToArray](./toarray/)() const | Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar. |
| static [Type](./type/)() |  |
## Açıklamalar


[NodeList](./) is returned by [SelectNodes()](../) and contains a collection of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.


[NodeList](./) koleksiyonunu bir "snapshot" koleksiyonu gibi ele alın. [NodeList](./) XPath sorgusu çalıştırıldığında düğümler aslında alınmadığı için "live" bir koleksiyon olarak başlar. Düğümler yalnızca erişildiğinde alınır ve bu sırada düğüm ve ondan önceki tüm düğümler önbelleğe alınarak bir "snapshot" koleksiyonu oluşturur.
## Örnekler



Bir Word belgesindeki tüm hiperlinkleri nasıl bulacağınızı ve ardından URL'lerini ve görüntülenen adlarını nasıl değiştireceğinizi gösterir.
```cpp
#include <system/text/regularexpressions/regex.h>
#include <Aspose.Words.Cpp/Model/Nodes/NodeType.h>
#include <Aspose.Words.Cpp/Model/Nodes/Node.h>
#include <Aspose.Words.Cpp/Model/Fields/Nodes/FieldStart.h>

#include "ApiExampleBase.h"

using namespace Aspose::Words::Fields;

namespace Aspose {

namespace Words {

namespace ApiExamples {

class ExReplaceHyperlinks : public ApiExampleBase
{
    typedef ExReplaceHyperlinks ThisType;
    typedef ApiExampleBase BaseType;

    typedef ::System::BaseTypesInfo<BaseType> ThisTypeBaseTypesInfo;
    RTTI_INFO_DECL();

public:

    void Fields();

protected:

    static const System::String& NewUrl();
    static const System::String& NewName();

};

class Hyperlink : public System::Object
{
    typedef Hyperlink ThisType;
    typedef System::Object BaseType;

    typedef ::System::BaseTypesInfo<BaseType> ThisTypeBaseTypesInfo;
    RTTI_INFO_DECL();

public:

    System::String get_Name();
    void set_Name(System::String value);
    System::String get_Target() const;
    void set_Target(System::String value);
    bool get_IsLocal() const;
    void set_IsLocal(bool value);

    Hyperlink(System::SharedPtr<Aspose::Words::Fields::FieldStart> fieldStart);

private:

    System::SharedPtr<Aspose::Words::Node> mFieldStart;
    System::SharedPtr<Aspose::Words::Node> mFieldSeparator;
    System::SharedPtr<Aspose::Words::Node> mFieldEnd;
    bool mIsLocal;
    System::String mTarget;

    static System::SharedPtr<System::Text::RegularExpressions::Regex>& gRegex();
    void UpdateFieldCode();
    static System::SharedPtr<Aspose::Words::Node> FindNextSibling(System::SharedPtr<Aspose::Words::Node> startNode, Aspose::Words::NodeType nodeType);
    static System::String GetTextSameParent(System::SharedPtr<Aspose::Words::Node> startNode, System::SharedPtr<Aspose::Words::Node> endNode);
    static void RemoveSameParent(System::SharedPtr<Aspose::Words::Node> startNode, System::SharedPtr<Aspose::Words::Node> endNode);

};

} // namespace ApiExamples
} // namespace Words
} // namespace Aspose
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
