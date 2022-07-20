---
title: BookmarkName
second_title: Aspose.Words لمراجع .NET API
description: الحصول على أو تعيين اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

الحصول على أو تعيين اسم إشارة مرجعية يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي.

```csharp
public string BookmarkName { get; set; }
```

### أمثلة

يوضح كيفية دمج جدول المحتويات وحقول التسلسل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكن لحقل جدول المحتويات إنشاء إدخال في جدول المحتويات الخاص به لكل حقل SEQ موجود في المستند.
// يحتوي كل إدخال على الفقرة التي تحتوي على حقل SEQ ،
// ورقم الصفحة التي يظهر عليها الحقل.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// تكوين حقل جدول المحتويات هذا للحصول على خاصية SequenceIdentifier بقيمة "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// تكوين حقل جدول المحتويات هذا لاختيار حقول SEQ الموجودة ضمن حدود إشارة مرجعية فقط
// المسمى "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// تعرض حقول SEQ عددًا يتزايد في كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بأعداد منفصلة لكل تسلسل مسمى فريد
// التي تم تحديدها بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
// أدخل حقل SEQ يحتوي على معرف تسلسل يطابق جدول المحتويات
// خاصية TableOfFiguresLabel. لن يُنشئ هذا الحقل إدخالاً في جدول المحتويات لأنه خارج
// حدود الإشارة المرجعية المعينة بواسطة "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFiguresLabel" في جدول المحتويات ويقع ضمن حدود الإشارة المرجعية.
// ستظهر الفقرة التي تحتوي على هذا الحقل في جدول المحتويات كإدخال.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// لا يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFiguresLabel" في جدول المحتويات ،
// وضمن حدود الإشارة المرجعية. لن تظهر فقرتها في جدول المحتويات كإدخال.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFiguresLabel" في جدول المحتويات ويقع ضمن حدود الإشارة المرجعية.
// يشير هذا الحقل أيضًا إلى إشارة مرجعية أخرى. ستظهر محتويات هذه الإشارة المرجعية في إدخال جدول المحتويات لحقل SEQ هذا.
// لن يعرض حقل SEQ نفسه محتويات تلك الإشارة المرجعية.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// قم بإنشاء إشارة مرجعية بالمحتويات التي ستظهر في إدخال جدول المحتويات بسبب حقل SEQ أعلاه الذي يشير إليه.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

### أنظر أيضا

* class [FieldSeq](../../fieldseq)
* مساحة الاسم [Aspose.Words.Fields](../../fieldseq)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->