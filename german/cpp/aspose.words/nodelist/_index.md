---
title: "Aspose::Words::NodeList Klasse"
linktitle: "NodeList"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeList Klasse. Stellt eine Sammlung von Knoten dar, die einer XPath-Abfrage entsprechen, die mit der Methode SelectNodes() ausgeführt wird. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 45000
url: /de/cpp/aspose.words/nodelist/
---
## NodeList class


Stellt eine Sammlung von Knoten dar, die einer mit der Methode [SelectNodes()](../) ausgeführten XPath‑Abfrage entsprechen. Weitere Informationen finden Sie im Dokumentationsartikel [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeList : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Count](./get_count/)() const | Gibt die Anzahl der Knoten in der Liste zurück. |
| [GetEnumerator](./getenumerator/)() override | Bietet eine einfache \"foreach\"-artige Iteration über die Sammlung von Knoten. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) const | Ruft einen Knoten am angegebenen Index ab. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeList](./nodelist/)(const System::SharedPtr\<Aspose::Words::NodeCollection\>\&) |  |
| [ToArray](./toarray/)() const | Kopiert alle Knoten aus der Sammlung in ein neues Knotenarray. |
| static [Type](./type/)() |  |
## Hinweise


[NodeList](./) is returned by [SelectNodes()](../) and contains a collection of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.


Behandeln Sie die [NodeList](./)-Sammlung als eine „Snapshot“-Sammlung. [NodeList](./) beginnt als eine „Live“-Sammlung, weil die Knoten beim Ausführen der XPath-Abfrage nicht tatsächlich abgerufen werden. Die Knoten werden erst beim Zugriff abgerufen und zu diesem Zeitpunkt werden der Knoten und alle vorhergehenden Knoten zwischengespeichert, wodurch eine „Snapshot“-Sammlung entsteht.
## Beispiele



Zeigt, wie man alle Hyperlinks in einem Word-Dokument findet und anschließend deren URLs und Anzeigenamen ändert.
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

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
