---
title: Aspose::Words::NodeList class
linktitle: NodeList
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeList class. Represents a collection of nodes matching an XPath query executed using the SelectNodes() method. To learn more, visit the  documentation article in C++.'
type: docs
weight: 45000
url: /cpp/aspose.words/nodelist/
---
## NodeList class


Represents a collection of nodes matching an XPath query executed using the [SelectNodes()](../) method. To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) documentation article.

```cpp
class NodeList : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Methods

| Method | Description |
| --- | --- |
| [get_Count](./get_count/)() const | Gets the number of nodes in the list. |
| [GetEnumerator](./getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) const | Retrieves a node at the given index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeList](./nodelist/)(const System::SharedPtr\<Aspose::Words::NodeCollection\>\&) |  |
| [ToArray](./toarray/)() const | Copies all nodes from the collection to a new array of nodes. |
| static [Type](./type/)() |  |
## Remarks


[NodeList](./) is returned by [SelectNodes()](../) and contains a collection of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.


Treat the [NodeList](./) collection as a "snapshot" collection. [NodeList](./) starts as a "live" collection because the nodes are not actually retrieved when the XPath query is run. The nodes are only retrieved upon access and at this time the node and all nodes that precede it are cached forming a "snapshot" collection.
## Examples



Shows how to find all hyperlinks in a Word document, and then change their URLs and display names. 
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

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
