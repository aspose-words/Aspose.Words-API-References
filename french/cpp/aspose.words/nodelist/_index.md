---
title: "Classe Aspose::Words::NodeList"
linktitle: "NodeList"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::NodeList. Représente une collection de nœuds correspondant à une requête XPath exécutée à l'aide de la méthode SelectNodes(). Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 45000
url: /fr/cpp/aspose.words/nodelist/
---
## NodeList class


Représente une collection de nœuds correspondant à une requête XPath exécutée à l'aide de la méthode [SelectNodes()](../). Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeList : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Count](./get_count/)() const | Obtient le nombre de nœuds dans la liste. |
| [GetEnumerator](./getenumerator/)() override | Fournit une itération simple de type "foreach" sur la collection de nœuds. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) const | Récupère un nœud à l'index donné. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeList](./nodelist/)(const System::SharedPtr\<Aspose::Words::NodeCollection\>\&) |  |
| [ToArray](./toarray/)() const | Copie tous les nœuds de la collection dans un nouveau tableau de nœuds. |
| static [Type](./type/)() |  |
## Remarques


[NodeList](./) is returned by [SelectNodes()](../) and contains a collection of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.


Traitez la collection [NodeList](./) comme une collection "snapshot". [NodeList](./) commence comme une collection "live" car les nœuds ne sont pas réellement récupérés lorsque la requête XPath est exécutée. Les nœuds ne sont récupérés qu'à l'accès et, à ce moment, le nœud et tous les nœuds qui le précèdent sont mis en cache, formant une collection "snapshot".
## Exemples



Montre comment trouver tous les hyperliens dans un document Word, puis modifier leurs URL et leurs noms d'affichage.
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

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
