---
title: "طريقة Aspose::Words::PageSetup::get_LineNumberRestartMode"
linktitle: "get_LineNumberRestartMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_LineNumberRestartMode. يحصل أو يعيّن طريقة تشغيل ترقيم الأسطر، أي ما إذا كان يبدأ من جديد في بداية صفحة أو قسم جديد أو يستمر بشكل مستمر في C++."
type: docs
weight: 25000
url: /ar/cpp/aspose.words/pagesetup/get_linenumberrestartmode/
---
## PageSetup::get_LineNumberRestartMode method


يحصل أو يعيّن طريقة تشغيل ترقيم الأسطر، أي ما إذا كان يبدأ من جديد في بداية صفحة أو قسم جديد أو يستمر بشكل مستمر.

```cpp
Aspose::Words::LineNumberRestartMode Aspose::Words::PageSetup::get_LineNumberRestartMode()
```


## أمثلة



يوضح كيفية تمكين ترقيم الأسطر لقسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// يمكننا استخدام كائن PageSetup الخاص بالقسم لعرض الأرقام إلى يسار أسطر نص القسم.
// هذا هو نفس السلوك كما هو في كائن List،
// ولكنه يغطي القسم بأكمله ولا يغيّر النص بأي شكل.
// سوف يعيد قسمنا تشغيل الترقيم في كل صفحة جديدة من 1 ويعرض الرقم،
// إذا كان مضاعفًا للعدد 3، على بعد 50pt إلى يسار السطر.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_LineStartingNumber(1);
pageSetup->set_LineNumberCountBy(3);
pageSetup->set_LineNumberRestartMode(Aspose::Words::LineNumberRestartMode::RestartPage);
pageSetup->set_LineNumberDistanceFromText(50.0);

for (int32_t i = 1; i <= 25; i++)
{
    builder->Writeln(System::String::Format(u"Line {0}.", i));
}

// سيتخطى عداد الأسطر أي فقرة تحتوي على العلامة "SuppressLineNumbers" مضبوطة على "true".
// هذه الفقرة في السطر الـ15، وهو مضاعف للعدد 3، وبالتالي عادةً ما يتم عرض رقم السطر.
// سيتجاهل عداد أسطر القسم هذا السطر أيضًا، ويعامل السطر التالي كالسطر الـ15،
// ويستمر العد من تلك النقطة فصاعدًا.
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(14)->get_ParagraphFormat()->set_SuppressLineNumbers(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.LineNumbers.docx");
```

## انظر أيضًا

* Enum [LineNumberRestartMode](../../linenumberrestartmode/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
