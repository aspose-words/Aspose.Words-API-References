---
title: "Aspose::Words::TabStopCollection::Add method"
linktitle: "Add"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TabStopCollection::Add method. يضيف أو يستبدل علامة تبويب في المجموعة في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/tabstopcollection/add/
---
## TabStopCollection::Add(const System::SharedPtr\<Aspose::Words::TabStop\>\&) method


يضيف أو يستبدل علامة تبويب في المجموعة.

```cpp
void Aspose::Words::TabStopCollection::Add(const System::SharedPtr<Aspose::Words::TabStop> &tabStop)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| tabStop | const System::SharedPtr\<Aspose::Words::TabStop\>\& | كائن tab stop للإضافة. |
## ملاحظات


إذا كان هناك tab stop موجود بالفعل في الموضع المحدد، فسيتم استبداله.

## أمثلة



يوضح كيفية إضافة علامات تبويب مخصصة إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// فيما يلي طريقتان لإضافة علامات تبويب إلى مجموعة علامات تبويب الفقرة عبر خاصية "ParagraphFormat".
// 1 -  إنشاء كائن "TabStop"، ثم إضافته إلى المجموعة:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  تمرير القيم لخصائص علامة تبويب جديدة إلى طريقة "Add":
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// إضافة علامات تبويب على بعد 5 سم إلى جميع الفقرات.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// كل حرف "tab" ينقل مؤشر المُنشئ إلى موقع علامة التبويب التالية.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## انظر أيضًا

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStopCollection::Add(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) method


يضيف أو يستبدل علامة تبويب في المجموعة.

```cpp
void Aspose::Words::TabStopCollection::Add(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| position | double | موضع (بالنقاط) حيث يتم إضافة علامة التبويب. |
| alignment | Aspose::Words::TabAlignment | قيمة [TabAlignment](../../tabalignment/) التي تحدد محاذاة النص عند علامة التبويب. |
| leader | Aspose::Words::TabLeader | قيمة [TabLeader](../../tableader/) التي تحدد نوع الخط القائد المعروض تحت حرف التبويب. |
## ملاحظات


إذا كان هناك tab stop موجود بالفعل في الموضع المحدد، فسيتم استبداله.

## أمثلة



يوضح كيفية إضافة علامات تبويب مخصصة إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// فيما يلي طريقتان لإضافة علامات تبويب إلى مجموعة علامات تبويب الفقرة عبر خاصية "ParagraphFormat".
// 1 -  إنشاء كائن "TabStop"، ثم إضافته إلى المجموعة:
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  تمرير القيم لخصائص علامة تبويب جديدة إلى طريقة "Add":
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// إضافة علامات تبويب على بعد 5 سم إلى جميع الفقرات.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// كل حرف "tab" ينقل مؤشر المُنشئ إلى موقع علامة التبويب التالية.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## انظر أيضًا

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
