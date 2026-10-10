---
title: "Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions منشئ"
linktitle: "RtfLoadOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions. يهيئ نسخة جديدة من هذه الفئة بالقيم الافتراضية في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions::RtfLoadOptions constructor


ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية.

```cpp
Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions()
```


## أمثلة



يوضح كيفية اكتشاف أحرف UTF-8 أثناء تحميل مستند RTF.
```cpp
// أنشئ كائن "RtfLoadOptions" لتعديل طريقة تحميل مستند RTF.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// عيّن خاصية "RecognizeUtf8Text" إلى "false" لتفترض أن المستند يستخدم مجموعة الأحرف ISO 8859-1
// ويحمّل كل حرف في المستند.
// عيّن خاصية "RecognizeUtf8Text" إلى "true" لتحليل أي أحرف ذات طول متغيّر قد تظهر في النص.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## انظر أيضًا

* Class [RtfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
