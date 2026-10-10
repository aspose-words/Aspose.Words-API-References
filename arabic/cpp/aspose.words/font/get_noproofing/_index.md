---
title: "طريقة Aspose::Words::Font::get_NoProofing"
linktitle: "get_NoProofing"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_NoProofing. صحيح عندما لا يجب فحص الأحرف المُنسقة إملائيًا في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words/font/get_noproofing/
---
## Font::get_NoProofing method


صحيح عندما لا يتم تدقيق إملائي للأحرف المنسقة.

```cpp
bool Aspose::Words::Font::get_NoProofing()
```


## أمثلة



يظهر كيفية منع النص من فحصه إملائيًا بواسطة Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// عادةً، يبرز Microsoft Word أخطاء الإملاء بخط أحمر متعرج.
// يمكننا إلغاء تعيين علامة "NoProofing" لإنشاء جزء من النص الذي
// يتجاوز مدقق الإملاء مع تعطيله تمامًا.
builder->get_Font()->set_NoProofing(true);

builder->Writeln(u"Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc->Save(get_ArtifactsDir() + u"Font.NoProofing.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
