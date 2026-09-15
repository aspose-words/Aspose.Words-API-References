---
title: "طريقة Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text"
linktitle: "get_RecognizeUtf8Text"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text. عندما يتم تعيينها إلى true، سيحاول اكتشاف أحرف UTF8، وسيتم الحفاظ عليها أثناء الاستيراد في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.loading/rtfloadoptions/get_recognizeutf8text/
---
## RtfLoadOptions::get_RecognizeUtf8Text method


عند تعيينه إلى **true**، سيحاول اكتشاف أحرف UTF8، وسيتم الحفاظ عليها أثناء الاستيراد.

```cpp
bool Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text() const
```

## ملاحظات


القيمة الافتراضية هي **false**.

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
