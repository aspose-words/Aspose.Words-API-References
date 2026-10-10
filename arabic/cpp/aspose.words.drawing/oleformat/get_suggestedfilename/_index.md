---
title: "طريقة Aspose::Words::Drawing::OleFormat::get_SuggestedFileName"
linktitle: "get_SuggestedFileName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::OleFormat::get_SuggestedFileName. يحصل على اسم الملف المقترح للكائن المضمن الحالي إذا أردت حفظه في ملف في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.drawing/oleformat/get_suggestedfilename/
---
## OleFormat::get_SuggestedFileName method


يحصل على اسم الملف المقترح للكائن المضمن الحالي إذا رغبت في حفظه في ملف.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SuggestedFileName()
```


## أمثلة



يظهر كيفية الحصول على اسم الملف المقترح لكائن OLE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE shape.rtf");

auto oleShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// يمكن لكائنات OLE توفير اسم ملف مقترح وامتداد،
// والتي يمكننا استخدامها عند حفظ محتويات الكائن في ملف على نظام الملفات المحلي.
System::String suggestedFileName = oleShape->get_OleFormat()->get_SuggestedFileName();

ASSERT_EQ(u"CSV.csv", suggestedFileName);

{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + suggestedFileName, System::IO::FileMode::Create);
    oleShape->get_OleFormat()->Save(fileStream);
}
```

## انظر أيضًا

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
