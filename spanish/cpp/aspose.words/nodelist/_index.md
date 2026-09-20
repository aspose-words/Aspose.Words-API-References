---
title: "Clase Aspose::Words::NodeList"
linktitle: "NodeList"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::NodeList. Representa una colección de nodos que coinciden con una consulta XPath ejecutada mediante el método SelectNodes(). Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 45000
url: /es/cpp/aspose.words/nodelist/
---
## NodeList class


Representa una colección de nodos que coinciden con una consulta XPath ejecutada mediante el método [SelectNodes()](../). Para obtener más información, visite el artículo de documentación de [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeList : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Count](./get_count/)() const | Obtiene el número de nodos en la lista. |
| [GetEnumerator](./getenumerator/)() override | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) const | Recupera un nodo en el índice dado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeList](./nodelist/)(const System::SharedPtr\<Aspose::Words::NodeCollection\>\&) |  |
| [ToArray](./toarray/)() const | Copia todos los nodos de la colección a una nueva matriz de nodos. |
| static [Type](./type/)() |  |
## Observaciones


[NodeList](./) is returned by [SelectNodes()](../) and contains a collection of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.


Trate la colección [NodeList](./) como una colección "snapshot". [NodeList](./) comienza como una colección "live" porque los nodos no se recuperan realmente cuando se ejecuta la consulta XPath. Los nodos solo se recuperan al acceder y en ese momento el nodo y todos los nodos que lo preceden se almacenan en caché formando una colección "snapshot".
## Ejemplos



Muestra cómo encontrar todos los hipervínculos en un documento Word y luego cambiar sus URL y nombres de visualización.
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

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
