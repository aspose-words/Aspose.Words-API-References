---
title: "Aspose::Words::NodeList class"
linktitle: "NodeList"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeList class. Представляет собой коллекцию узлов, соответствующих XPath‑запросу, выполненному с помощью метода SelectNodes(). Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 45000
url: /ru/cpp/aspose.words/nodelist/
---
## NodeList class


Представляет коллекцию узлов, соответствующих запросу XPath, выполненному с помощью метода [SelectNodes()](../). Чтобы узнать больше, посетите статью документации [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeList : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Count](./get_count/)() const | Получает количество узлов в списке. |
| [GetEnumerator](./getenumerator/)() override | Предоставляет простую итерацию в стиле "foreach" по коллекции узлов. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) const | Получает узел по заданному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeList](./nodelist/)(const System::SharedPtr\<Aspose::Words::NodeCollection\>\&) |  |
| [ToArray](./toarray/)() const | Копирует все узлы из коллекции в новый массив узлов. |
| static [Type](./type/)() |  |
## Примечания


[NodeList](./) is returned by [SelectNodes()](../) and contains a collection of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.


Обрабатывайте коллекцию [NodeList](./) как коллекцию "snapshot". [NodeList](./) начинается как коллекция "live", потому что узлы фактически не извлекаются при выполнении XPath‑запроса. Узлы извлекаются только при доступе, и в этот момент узел и все предшествующие ему узлы кэшируются, образуя коллекцию "snapshot".
## Примеры



Показывает, как найти все гиперссылки в документе Word, а затем изменить их URL‑адреса и отображаемые имена.
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

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
