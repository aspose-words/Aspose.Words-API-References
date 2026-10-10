---
title: "طريقة Aspose::Words::Math::OfficeMath::GetMathRenderer"
linktitle: "GetMathRenderer"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Math::OfficeMath::GetMathRenderer. ينشئ ويعيد كائنًا يمكن استخدامه لتصوير هذه المعادلة كصورة في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath::GetMathRenderer method


ينشئ ويرجع كائنًا يمكن استخدامه لتصوير هذه المعادلة كصورة.

```cpp
System::SharedPtr<Aspose::Words::Rendering::OfficeMathRenderer> Aspose::Words::Math::OfficeMath::GetMathRenderer()
```


### ReturnValue

كائن المُعالج لهذه المعادلة.
## ملاحظات


هذه الطريقة تستدعي فقط مُنشئ [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/) وتمرّر هذا الكائن كمعامل.

## أمثلة



يظهر كيفية تصيير كائن Office [Math](../../) إلى ملف صورة في نظام الملفات المحلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// أنشئ كائن "ImageSaveOptions" لتمريره إلى طريقة "Save" الخاصة بالمُعالج العقدة لتعديل
// كيفية تصييره لعقدة OfficeMath إلى صورة.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// اضبط خاصية "Scale" إلى 5 لتصوير الكائن بمقاس يساوي خمسة أضعاف حجمه الأصلي.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## انظر أيضًا

* Class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
