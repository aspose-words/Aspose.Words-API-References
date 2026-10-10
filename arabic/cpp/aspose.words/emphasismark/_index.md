---
title: "Aspose::Words::EmphasisMark enum"
linktitle: "EmphasisMark"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::EmphasisMark enum. يحدد الأنواع الممكنة لعلامة التأكيد في C++."
type: docs
weight: 89000
url: /ar/cpp/aspose.words/emphasismark/
---
## EmphasisMark enum


يحدد الأنواع الممكنة لعلامة التشديد.

```cpp
enum class EmphasisMark
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | لا توجد علامة تأكيد. |
| OverSolidCircle | 1 | علامة التأكيد هي دائرة سوداء صلبة تُعرض فوق النص. |
| OverComma | 2 | علامة التأكيد هي حرف فاصلة يُعرض فوق النص. |
| OverWhiteCircle | 3 | علامة التأكيد هي دائرة بيضاء فارغة تُعرض فوق النص. |
| UnderSolidCircle | 4 | علامة التأكيد هي دائرة سوداء صلبة تُعرض أسفل النص. |


## أمثلة



يظهر كيفية إضافة حرف إضافي يُعرض فوق/تحت حرف الشكل.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// الأنواع الممكنة لعلامة التأكيد:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
