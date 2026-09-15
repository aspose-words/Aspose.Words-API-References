---
title: "Aspose::Words::Fonts::FontSubstitutionSettings class"
linktitle: "FontSubstitutionSettings"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fonts::FontSubstitutionSettings. يحدد إعدادات آلية استبدال الخط. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class


يحدد إعدادات آلية استبدال الخط. لمزيد من المعلومات، قم بزيارة مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSubstitutionSettings : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DefaultFontSubstitution](./get_defaultfontsubstitution/)() const | [الإعدادات](../../aspose.words.settings/) المتعلقة بقاعدة استبدال الخط الافتراضية. |
| [get_FontConfigSubstitution](./get_fontconfigsubstitution/)() const | [الإعدادات](../../aspose.words.settings/) المتعلقة بقاعدة استبدال تكوين الخط. |
| [get_FontInfoSubstitution](./get_fontinfosubstitution/)() const | [الإعدادات](../../aspose.words.settings/) المتعلقة بقاعدة استبدال معلومات الخط. |
| [get_FontNameSubstitution](./get_fontnamesubstitution/)() const | [الإعدادات](../../aspose.words.settings/) المتعلقة بقاعدة استبدال اسم الخط. |
| [get_TableSubstitution](./get_tablesubstitution/)() const | [الإعدادات](../../aspose.words.settings/) المتعلقة بقاعدة استبدال الجدول. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## ملاحظات


[Font](../../aspose.words/font/) substitution process consists of several rules which are checked one by one in specific order. If the first rule can't resolve the font then second rule is checked and so on.

ترتيب القواعد كما يلي:1. قاعدة استبدال اسم [الخط](../../aspose.words/font/) (مفعلة افتراضيًا)
1. قاعدة استبدال تكوين [الخط](../../aspose.words/font/) (معطلة افتراضيًا)
1. قاعدة استبدال الجدول (مفعلة افتراضيًا)
1. قاعدة استبدال معلومات [الخط](../../aspose.words/font/) (مفعلة افتراضيًا)
1. قاعدة الخط الافتراضي (مفعلة افتراضيًا)



لاحظ أن قاعدة استبدال معلومات الخط ستحل دائمًا الخط إذا كان [معلومات الخط](../fontinfo/) متاحًا وستتجاوز قاعدة الخط الافتراضي. إذا كنت تريد استخدام قاعدة الخط الافتراضي، يجب عليك تعطيل قاعدة استبدال معلومات الخط.

لاحظ أن قاعدة استبدال تكوين الخط ستحل الخط في معظم الحالات وبالتالي تتجاوز جميع القواعد الأخرى.

## أمثلة



يظهر كيفية الوصول إلى مصدر خطوط النظام في المستند وتعيين بدائل الخطوط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// بشكل افتراضي، يحتوي المستند الفارغ دائمًا على مصدر خطوط النظام.
ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());

auto systemFontSource = System::ExplicitCast<Aspose::Words::Fonts::SystemFontSource>(doc->get_FontSettings()->GetFontsSources()->idx_get(0));
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, systemFontSource->get_Type());
ASSERT_EQ(0, systemFontSource->get_Priority());

System::PlatformID pid = System::Environment::get_OSVersion().get_Platform();
bool isWindows = (pid == System::PlatformID::Win32NT) || (pid == System::PlatformID::Win32S) || (pid == System::PlatformID::Win32Windows) || (pid == System::PlatformID::WinCE);
if (isWindows)
{
    const System::String fontsPath = u"C:\\WINDOWS\\Fonts";
    System::String actual = System::Default<System::String>();
    System::String condExpression = Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders()->LINQ_FirstOrDefault();
    if (condExpression != nullptr)
    {
        actual = condExpression.ToLower();
    }
    ASSERT_EQ(fontsPath.ToLower(), actual);
}

for (System::String systemFontFolder : Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders())
{
    std::cout << systemFontFolder << std::endl;
}

// حدد خطًا موجودًا في دليل خطوط Windows كبديل لخط غير موجود.
doc->get_FontSettings()->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Kreon-Regular", System::MakeArray<System::String>({u"Calibri"}));

ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_ToArray()->Contains(u"Calibri"));

// بدلاً من ذلك، يمكننا إضافة مصدر خطوط مجلد حيث يحتوي المجلد المقابل على الخط.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({systemFontSource, folderFontSource}));
ASSERT_EQ(2, doc->get_FontSettings()->GetFontsSources()->get_Length());

// إعادة ضبط مصادر الخطوط لا يزال يتركنا مع مصدر خطوط النظام بالإضافة إلى بدائلنا.
doc->get_FontSettings()->ResetFontSources();

ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, doc->get_FontSettings()->GetFontsSources()->idx_get(0)->get_Type());
ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_FontNameSubstitution()->get_Enabled());
```

## انظر أيضًا

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
