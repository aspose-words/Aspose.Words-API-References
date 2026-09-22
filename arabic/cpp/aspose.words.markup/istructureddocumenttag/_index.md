---
title: "Aspose::Words::Markup::IStructuredDocumentTag واجهة"
linktitle: "IStructuredDocumentTag"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag واجهة. واجهة لتحديد بيانات مشتركة لـ StructuredDocumentTag و StructuredDocumentTagRangeStart في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface


واجهة لتحديد بيانات مشتركة لـ [StructuredDocumentTag](../structureddocumenttag/) و [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).

```cpp
class IStructuredDocumentTag : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [get_Appearance](./get_appearance/)() | يحصل أو يضبط مظهر علامة المستند المهيكلة. |
| virtual [get_Color](./get_color/)() | يحصل أو يضبط لون علامة المستند المهيكلة. |
| virtual [get_Id](./get_id/)() | يحدد معرفًا رقميًا فريدًا للقراءة فقط ومستمرًا لهذا **SDT**. |
| virtual [get_IsMultiSection](./get_ismultisection/)() | يرجع true إذا كانت هذه الحالة علامة مستند مهيكلة بنطاق (متعددة الأقسام). |
| virtual [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() | يحدد ما إذا كان محتوى هذا **SDT** سيُفسَّر على أنه يحتوي نصًا نائبًا (على عكس محتويات النص العادية داخل الـ SDT). إذا تم تعيينه إلى true، ستستأنف هذه الحالة (عرض النص النائب) عند فتح هذا المستند. |
| virtual [get_Level](./get_level/)() const | يحصل على المستوى الذي يحدث فيه هذا **SDT** في شجرة المستند. |
| virtual [get_LockContentControl](./get_lockcontentcontrol/)() | عند تعيينه إلى true، سيمنع هذا الخاصية المستخدم من حذف هذا **SDT**. |
| virtual [get_LockContents](./get_lockcontents/)() | عند تعيينه إلى true، سيمنع هذا الخاصية المستخدم من تعديل محتويات هذا **SDT**. |
| virtual [get_Node](./get_node/)() | يرجع كائن [Node](../../aspose.words/node/) الذي يطبق هذه الواجهة. |
| virtual [get_Placeholder](./get_placeholder/)() | يحصل على [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) الذي يحتوي على نص نائب يجب عرضه عندما تكون محتويات تشغيل الـ SDT فارغة، أو يكون عنصر XML المرتبط فارغًا كما هو محدد عبر عنصر [XmlMapping](./get_xmlmapping/)، أو يكون عنصر [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) true. |
| virtual [get_PlaceholderName](./get_placeholdername/)() | يحصل أو يضبط اسم [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) الذي يحتوي على نص نائب. |
| virtual [get_SdtType](./get_sdttype/)() | يحصل على نوع هذه **Structured document tag**. |
| virtual [get_Tag](./get_tag/)() const | يحدد علامة مرتبطة بعقدة الـ SDT الحالية. لا يمكن أن تكون null. |
| virtual [get_Title](./get_title/)() const | يحدد الاسم الودي المرتبط بهذا **SDT**. لا يمكن أن يكون null. |
| virtual [get_WordOpenXML](./get_wordopenxml/)() | يحصل على سلسلة تمثل XML الموجود داخل العقدة بصيغة [FlatOpc](../../aspose.words/saveformat/). |
| virtual [get_XmlMapping](./get_xmlmapping/)() | يحصل على كائن يمثل تخطيط هذه علامة المستند المهيكلة إلى بيانات XML في جزء XML مخصص للمستند الحالي. |
| virtual [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | يرجع مجموعة حية من العقد الفرعية التي تطابق الأنواع المحددة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RemoveSelfOnly](./removeselfonly/)() | يزيل عقدة الـ SDT هذه فقط، لكنه يحتفظ بمحتواها داخل شجرة المستند. |
| virtual [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) | مُعيّن لـ [Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance](./get_appearance/). |
| virtual [set_Color](./set_color/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Markup::IStructuredDocumentTag::get_Color](./get_color/). |
| virtual [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) | مُعيّن لـ [Aspose::Words::Markup::IStructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| virtual [set_LockContentControl](./set_lockcontentcontrol/)(bool) | مُعيّن لـ [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| virtual [set_LockContents](./set_lockcontents/)(bool) | مُعيّن لـ [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| virtual [set_PlaceholderName](./set_placeholdername/)(System::String) | مُعيّن لـ [Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| virtual [set_Tag](./set_tag/)(System::String) | مُعيّن لـ [Aspose::Words::Markup::IStructuredDocumentTag::get_Tag](./get_tag/). |
| virtual [set_Title](./set_title/)(System::String) | المُعيّن لـ [Aspose::Words::Markup::IStructuredDocumentTag::get_Title](./get_title/). |
| static [Type](./type/)() |  |

## أمثلة



يُظهر كيفية إزالة علامة المستند المُنظمة، لكنه يحتفظ بالمحتوى داخلها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// توفر هذه المجموعة واجهة موحدة للوصول إلى العلامات المُنظمة ذات النطاق وغير ذات النطاق.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// هنا يمكننا الحصول على العقد الفرعية من الواجهة المشتركة للعلامات المُنظمة ذات النطاق وغير ذات النطاق.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## انظر أيضًا

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
