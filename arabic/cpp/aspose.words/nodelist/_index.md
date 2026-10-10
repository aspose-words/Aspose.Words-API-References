---
title: "فئة Aspose::Words::NodeList"
linktitle: "NodeList"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::NodeList. تمثل مجموعة من العقد التي تطابق استعلام XPath يتم تنفيذه باستخدام طريقة SelectNodes(). لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 45000
url: /ar/cpp/aspose.words/nodelist/
---
## NodeList class


يمثل مجموعة من العقد التي تطابق استعلام XPath يتم تنفيذه باستخدام طريقة [SelectNodes()](../). لمعرفة المزيد، زر مقالة الوثائق [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeList : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Count](./get_count/)() const | يحصل على عدد العقد في القائمة. |
| [GetEnumerator](./getenumerator/)() override | يوفر تكرارًا بسيطًا بنمط "foreach" على مجموعة العقد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) const | يسترجع عقدة في الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeList](./nodelist/)(const System::SharedPtr\<Aspose::Words::NodeCollection\>\&) |  |
| [ToArray](./toarray/)() const | ينسخ جميع العقد من المجموعة إلى مصفوفة جديدة من العقد. |
| static [Type](./type/)() |  |
## ملاحظات


[NodeList](./) is returned by [SelectNodes()](../) and contains a collection of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.


عامل مجموعة [NodeList](./) كأنها مجموعة \"snapshot\". تبدأ مجموعة [NodeList](./) كمجموعة \"live\" لأن العقد لا يتم جلبها فعليًا عند تشغيل استعلام XPath. يتم جلب العقد فقط عند الوصول إليها وفي ذلك الوقت تُخزن العقدة وجميع العقد التي تسبقها في الذاكرة لتشكيل مجموعة \"snapshot\".
## أمثلة



يوضح كيفية العثور على جميع الروابط التشعبية في مستند Word، ثم تغيير عناوين URL الخاصة بها وأسماء العرض.
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

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
