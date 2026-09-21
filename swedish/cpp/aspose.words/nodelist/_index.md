---
title: "Aspose::Words::NodeList-klass"
linktitle: "NodeList"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::NodeList-klass. Representerar en samling noder som matchar en XPath‑fråga som körs med SelectNodes()-metoden. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 45000
url: /sv/cpp/aspose.words/nodelist/
---
## NodeList class


Representerar en samling noder som matchar en XPath-fråga utförd med metoden [SelectNodes()](../). För att lära dig mer, besök dokumentationsartikeln [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) i dokumentationen.

```cpp
class NodeList : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Count](./get_count/)() const | Hämtar antalet noder i listan. |
| [GetEnumerator](./getenumerator/)() override | Tillhandahåller en enkel "foreach"‑liknande iteration över samlingen av noder. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) const | Hämtar en nod vid det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeList](./nodelist/)(const System::SharedPtr\<Aspose::Words::NodeCollection\>\&) |  |
| [ToArray](./toarray/)() const | Kopierar alla noder från samlingen till en ny nodarray. |
| static [Type](./type/)() |  |
## Anmärkningar


[NodeList](./) is returned by [SelectNodes()](../) and contains a collection of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.


Behandla [NodeList](./)-samlingen som en "snapshot"-samling. [NodeList](./) startar som en "live"-samling eftersom noderna faktiskt inte hämtas när XPath‑frågan körs. Noderna hämtas först vid åtkomst och vid den tidpunkten cachas noden och alla föregående noder, vilket bildar en "snapshot"-samling.
## Exempel



Visar hur man hittar alla hyperlänkar i ett Word‑dokument och sedan ändrar deras URL:er och visningsnamn.
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

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
