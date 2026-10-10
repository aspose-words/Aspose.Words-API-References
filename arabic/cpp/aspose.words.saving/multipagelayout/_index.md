---
title: "Aspose::Words::Saving::MultiPageLayout class"
linktitle: "MultiPageLayout"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::MultiPageLayout class. يحدد تخطيطًا لتحويل صفحات متعددة إلى مخرج واحد في C++."
type: docs
weight: 14500
url: /ar/cpp/aspose.words.saving/multipagelayout/
---
## MultiPageLayout class


يحدد تخطيطًا لتصيير صفحات متعددة في مخرج واحد.

```cpp
class MultiPageLayout : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | يحصل على لون خلفية المخرج. القيمة الافتراضية هي **Empty**. |
| [get_BorderColor](./get_bordercolor/)() | يحصل على لون حد الصفحات. القيمة الافتراضية هي **Empty**. |
| [get_BorderWidth](./get_borderwidth/)() const | يحصل على عرض حد الصفحات. القيمة الافتراضية هي 0. |
| [GetType](./gettype/)() const override |  |
| static [Grid](./grid/)(int32_t, float, float) | ينشئ تخطيطًا تُعرض فيه الصفحات من اليسار إلى اليمين، من الأعلى إلى الأسفل، في شبكة بعدد الأعمدة المحدد. |
| static [Horizontal](./horizontal/)(float) | ينشئ تخطيطًا تُعرض فيه جميع الصفحات المحددة أفقيًا جنبًا إلى جنب، من اليسار إلى اليمين، في مخرج واحد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | يضبط لون خلفية المخرج. القيمة الافتراضية هي **Empty**. |
| [set_BorderColor](./set_bordercolor/)(System::Drawing::Color) | يضبط لون حد الصفحات. القيمة الافتراضية هي **Empty**. |
| [set_BorderWidth](./set_borderwidth/)(float) | يضبط عرض حد الصفحات. القيمة الافتراضية هي 0. |
| static [SinglePage](./singlepage/)() | ينشئ تخطيطًا يعرض فقط أول صفحة من الصفحات المحددة. |
| static [TiffFrames](./tiffframes/)() | ينشئ تخطيطًا حيث يتم عرض كل صفحة كإطار منفصل في صورة TIFF متعددة الإطارات. ينطبق فقط على صيغ صور TIFF. |
| static [Type](./type/)() |  |
| static [Vertical](./vertical/)(float) | ينشئ تخطيطًا حيث يتم عرض جميع الصفحات المحددة عموديًا واحدةً تحت الأخرى في مخرجات واحدة. |

## أمثلة



يظهر كيفية حفظ المستند كصورة JPG مع إعدادات تخطيط متعدد الصفحات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// إعداد تخطيط شبكة مع:
// - 3 أعمدة لكل صف.
// - 10 نقاط مسافة بين الصفحات (أفقية وعمودية).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// تخطيطات بديلة:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// تخصيص الخلفية والحد.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
