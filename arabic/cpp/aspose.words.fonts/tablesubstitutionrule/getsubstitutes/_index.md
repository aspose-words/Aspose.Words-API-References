---
title: "Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes method"
linktitle: "GetSubstitutes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes method. يُرجِع مصفوفة تحتوي على أسماء الخطوط البديلة للخط الأصلي المحدد في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fonts/tablesubstitutionrule/getsubstitutes/
---
## TableSubstitutionRule::GetSubstitutes method


يرجع مصفوفة تحتوي على أسماء الخطوط البديلة للخط الأصلي المحدد.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerable<System::String>> Aspose::Words::Fonts::TableSubstitutionRule::GetSubstitutes(const System::String &originalFontName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| originalFontName | const System::String\& | اسم الخط الأصلي. |

### ReturnValue

قائمة بأسماء الخطوط البديلة.

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


يوضح كيفية العمل مع جداول استبدال الخطوط المخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// أنشئ قاعدة استبدال جدول جديدة وحمّل جدول استبدال الخطوط الافتراضي لنظام Windows.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// إذا اخترنا الخطوط حصريًا من مجلدنا، سنحتاج إلى جدول استبدال مخصص.
// لن نتمكن بعد الآن من الوصول إلى خطوط Microsoft Windows،
// مثل \"Arial\" أو \"Times New Roman\" لأنها غير موجودة في مجلد الخطوط الجديد لدينا.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// أدناه طريقتان لتحميل جدول الاستبدال من ملف في نظام الملفات المحلي.
// 1 -  من تدفق:
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  مباشرةً من ملف:
tableSubstitutionRule->Load(get_MyDir() + u"Font substitution rules.xml");

// بما أننا لم نعد نمتلك إمكانية الوصول إلى \"Arial\"، سيحاول جدول الخطوط أولاً استبداله بـ \"Nonexistent Font\".
// لا نمتلك هذا الخط لذا سيتحول إلى الاستبدال التالي، \"Kreon\"، الموجود في مجلد \"MyFonts\".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// يمكننا توسيع هذا الجدول برمجياً. سنضيف مدخلاً يستبدل \"Times New Roman\" بـ \"Arvo\".
ASSERT_TRUE(System::TestTools::IsNull(tableSubstitutionRule->GetSubstitutes(u"Times New Roman")));
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// يمكننا إضافة استبدال احتياطي ثانوي لمدخل خط موجود باستخدام AddSubstitutes().
// في حال عدم توفر \"Arvo\"، سيبحث جدولنا عن \"M+ 2m\" كخيار استبدال ثانٍ.
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// يمكن لـ SetSubstitutes() تعيين قائمة جديدة من الخطوط البديلة لخط معين.
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// كتابة النص بخطوط لا نمتلك إمكانية الوصول إليها سيؤدي إلى تطبيق قواعد الاستبدال الخاصة بنا.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## انظر أيضًا

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
