---
title: "طريقة Aspose::Words::Fields::FieldSeq::get_BookmarkName"
linktitle: "طريقة Aspose::Words::Fields::FieldAsk::set_DefaultResponse"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldSeq::get_BookmarkName. يحصل على أو يضبط اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldseq/get_bookmarkname/
---
## FieldSeq::get_BookmarkName method


يحصل أو يعيّن اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_BookmarkName()
```


## أمثلة



يعرض كيفية دمج جدول المحتويات وحقول التسلسل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// يمكن لحقل TOC إنشاء إدخال في جدول محتوياته لكل حقل SEQ يُعثر عليه في المستند.
// كل إدخال يحتوي على الفقرة التي تحتوي على حقل SEQ،
// والرقم الصفحة التي يظهر فيها الحقل.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// قم بتكوين حقل TOC هذا ليحتوي على خاصية SequenceIdentifier بقيمة "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// قم بتكوين حقل TOC هذا ليلتقط فقط حقول SEQ التي تقع ضمن حدود إشارة مرجعية
// المسماة "TOCBookmark".
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// حقول SEQ تعرض عدًّا يزداد في كل حقل SEQ.
// هذه الحقول تحافظ أيضًا على عدّات منفصلة لكل تسلسل مسمى فريد
// مُحدَّد بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
// أدرج حقل SEQ يحتوي على معرف تسلسل يتطابق مع TOC's
// خاصية TableOfFiguresLabel. هذا الحقل لن ينشئ إدخالًا في TOC لأنه خارج
// حدود الإشارة المرجعية المحددة بواسطة "BookmarkName".
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// تطابق تسلسل حقل SEQ هذا خاصية "TableOfFiguresLabel" للـ TOC وهو ضمن حدود الإشارة المرجعية.
// الفقرة التي تحتوي على هذا الحقل ستظهر في TOC كإدخال.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// تسلسل حقل SEQ هذا لا يتطابق مع خاصية "TableOfFiguresLabel" للـ TOC،
// وهو ضمن حدود الإشارة المرجعية. فقرتها لن تظهر في TOC كإدخال.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// تطابق تسلسل حقل SEQ هذا خاصية "TableOfFiguresLabel" للـ TOC وهو ضمن حدود الإشارة المرجعية.
// هذا الحقل يشير أيضًا إلى إشارة مرجعية أخرى. محتويات تلك الإشارة المرجعية ستظهر في إدخال TOC لهذا الحقل SEQ.
// حقل SEQ نفسه لن يعرض محتويات تلك الإشارة المرجعية.
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// أنشئ إشارة مرجعية بمحتويات ستظهر في إدخال TOC بسبب إشارة حقل SEQ أعلاه إليها.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## انظر أيضًا

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
