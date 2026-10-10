---
title: "Aspose::Words::Drawing::PatternType enum"
linktitle: "PatternType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::PatternType enum. يحدد نمط التعبئة الذي سيُستخدم لملء شكل في C++."
type: docs
weight: 31000
url: /ar/cpp/aspose.words.drawing/patterntype/
---
## PatternType enum


يحدد نمط التعبئة الذي سيُستخدم لملء الشكل.

```cpp
enum class PatternType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | -1 | بدون نمط. |
| Percent10 | 1 | 10% من لون المقدمة. |
| Percent20 | 2 | 20% من لون المقدمة. |
| Percent25 | 3 | 25% من لون المقدمة. |
| Percent30 | 4 | 30% من لون المقدمة. |
| Percent40 | 5 | 40% من لون المقدمة |
| Percent50 | 6 | 50% من لون المقدمة |
| Percent5 | 7 | 5% من لون المقدمة. |
| Percent60 | 8 | 60% من لون المقدمة. |
| Percent70 | 9 | 70% من لون المقدمة. |
| Percent75 | 10 | 75% من لون المقدمة. |
| Percent80 | 11 | 80% من لون المقدمة. |
| Percent90 | 12 | 90% من لون المقدمة. |
| Cross | 13 | صليب. |
| مائل سفلي غامق | 14 | مائل سفلي غامق. |
| أفقي غامق | 15 | أفقي غامق. |
| مائل صاعد غامق | 16 | مائل صاعد غامق. |
| عمودي غامق | 17 | عمودي غامق. |
| مائل سفلي متقطع | 18 | مائل سفلي متقطع. |
| أفقي متقطع | 19 | أفقي متقطع. |
| مائل صاعد متقطع | 20 | مائل صاعد متقطع. |
| عمودي متقطع | 21 | عمودي متقطع. |
| قالب مائل | 22 | قالب مائل. |
| صليب مائل | 23 | صليب مائل. |
| ثقب | 24 | ثقب نمطي. |
| ماسة منقطة | 25 | ماسة منقطة. |
| شبكة منقطة | 26 | شبكة منقطة. |
| قطري نزولي | 27 | قطري نزولي. |
| أفقي | 28 | أفقي. |
| قالب أفقي | 29 | قالب أفقي. |
| لوحة شطرنجية كبيرة | 30 | لوحة شطرنجية كبيرة. |
| قُرص كبير | 31 | قُرص كبير. |
| شبكة كبيرة | 32 | شبكة كبيرة. |
| قطري نزولي خفيف | 33 | قطري نزولي خفيف. |
| أفقي خفيف | 34 | أفقي خفيف. |
| قطري صاعد خفيف | 36 | قطري صاعد خفيف. |
| عمودي خفيف | 37 | عمودي خفيف. |
| أفقي ضيق | 38 | أفقي ضيق. |
| عمودي ضيق | 39 | عمودي ضيق. |
| OutlinedDiamond | 40 | معين محدد. |
| قماش مخطط | 41 | قماش مخطط. |
| قالب | 42 | قالب. |
| SmallCheckerBoard | 43 | لوحة شطرنج صغيرة. |
| SmallConfetti | 44 | قصاصات صغيرة. |
| SmallGrid | 45 | شبكة صغيرة. |
| SolidDiamond | 46 | معين صلب. |
| كرة | 47 | كرة. |
| شبكة | 48 | شبكة. |
| UpwardDiagonal | 49 | قطري صاعد. |
| عمودي | 50 | عمودي. |
| Wave | 51 | موجة. |
| نسيج | 52 | نسيج. |
| WideDownwardDiagonal | 53 | قطري هابط واسع. |
| WideUpwardDiagonal | 54 | قطر مائل عريض. |
| ZigZag | 55 | متعرج. |


## أمثلة



يوضح كيفية تعيين نمط لشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// هناك عدة طرق لتحديد تعبئة بنمط.
// 1 -  تطبيق النمط على تعبئة الشكل:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  تطبيق النمط مع ألوان المقدمة والخلفية على تعبئة الشكل:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
