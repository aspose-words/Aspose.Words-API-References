---
title: "Aspose::Words::Framesets::Frameset class"
linktitle: "Frameset"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Framesets::Frameset class. يمثل صفحة إطارات أو إطارًا واحدًا على صفحة إطارات. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.framesets/frameset/
---
## Frameset class


يمثل صفحة إطارات أو إطارًا واحدًا على صفحة إطارات. لمعرفة المزيد، زر مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Frameset : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Frameset](./frameset/)() |  |
| [get_ChildFramesets](./get_childframesets/)() const | يحصل على مجموعة الإطارات الفرعية وصفحات الإطارات. |
| [get_FrameDefaultUrl](./get_framedefaulturl/)() | يحصل أو يعيّن عنوان URL للصفحة الويب أو اسم ملف المستند لعرضه في هذا الإطار. |
| [get_IsFrameLinkToFile](./get_isframelinktofile/)() | يحصل أو يعيّن قيمة تشير إلى ما إذا كان عنوان URL للصفحة الويب أو اسم ملف المستند المحدد في الخاصية [FrameDefaultUrl](./get_framedefaulturl/) هو مورد خارجي يرتبط به الإطار. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FrameDefaultUrl](./set_framedefaulturl/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl](./get_framedefaulturl/). |
| [set_IsFrameLinkToFile](./set_isframelinktofile/)(bool) | المُعيّن لـ [Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile](./get_isframelinktofile/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية الوصول إلى الإطارات داخل الصفحة.
```cpp
// المستند يحتوي على عدة إطارات مع روابط إلى مستندات أخرى.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Frameset.docx");

ASSERT_EQ(3, doc->get_Frameset()->get_ChildFramesets()->get_Count());
// يمكننا التحقق من عنوان URL الافتراضي (عنوان URL لصفحة ويب أو مستند محلي) أو ما إذا كان الإطار موردًا خارجيًا.
ASSERT_EQ(u"https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_FrameDefaultUrl());
ASSERT_TRUE(doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_IsFrameLinkToFile());

ASSERT_EQ(u"Document.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_FrameDefaultUrl());
ASSERT_FALSE(doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_IsFrameLinkToFile());

// تغيير الخصائص لإحدى إطاراتنا.
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_FrameDefaultUrl(u"https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_IsFrameLinkToFile(false);
```

## انظر أيضًا

* Namespace [Aspose::Words::Framesets](../)
* Library [Aspose.Words for C++](../../)
