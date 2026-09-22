---
title: "طريقة Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl"
linktitle: "get_FrameDefaultUrl"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl. يحصل على أو يعيّن عنوان URL لصفحة الويب أو اسم ملف المستند لعرضه في هذا الإطار في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.framesets/frameset/get_framedefaulturl/
---
## Frameset::get_FrameDefaultUrl method


يحصل أو يعيّن عنوان URL للصفحة الويب أو اسم ملف المستند لعرضه في هذا الإطار.

```cpp
System::String Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl()
```


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

* Class [Frameset](../)
* Namespace [Aspose::Words::Framesets](../../)
* Library [Aspose.Words for C++](../../../)
