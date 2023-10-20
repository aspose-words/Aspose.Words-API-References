---
title: FieldSeq.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words لـ .NET
description: FieldSeq BookmarkName ملكية. الحصول على أو تعيين اسم الإشارة المرجعية التي تشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

الحصول على أو تعيين اسم الإشارة المرجعية التي تشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي.

```csharp
public string BookmarkName { get; set; }
```

## أمثلة

يوضح كيفية الجمع بين جدول المحتويات وحقول التسلسل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكن لحقل جدول المحتويات إنشاء إدخال في جدول محتوياته لكل حقل تسلسلي موجود في المستند.
// يحتوي كل إدخال على الفقرة التي تحتوي على حقل SEQ،
// ورقم الصفحة التي يظهر عليها الحقل.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// قم بتكوين حقل جدول المحتويات هذا ليحتوي على خاصية SequenceIdentifier بقيمة "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// قم بتكوين حقل جدول المحتويات هذا لالتقاط حقول SEQ الموجودة ضمن حدود الإشارة المرجعية فقط
// اسمه "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

تعرض حقول SEQ عددًا يتزايد في كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بأعداد منفصلة لكل تسلسل مسمى فريد
// تم تحديده بواسطة خاصية "SequenceIdentifier" الخاصة بحقل SEQ.
// أدخل حقل SEQ الذي يحتوي على معرف تسلسل يطابق جدول المحتويات
// خاصية TableOfFigersLabel. لن يقوم هذا الحقل بإنشاء إدخال في جدول المحتويات لأنه موجود بالخارج
// حدود الإشارة المرجعية المعينة بواسطة "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFigursLabel" الخاصة بجدول المحتويات ويقع ضمن حدود الإشارة المرجعية.
// ستظهر الفقرة التي تحتوي على هذا الحقل في جدول المحتويات كمدخل.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// تسلسل حقل SEQ هذا لا يتطابق مع خاصية "TableOfFigersLabel" الخاصة بجدول المحتويات،
// ويقع ضمن حدود الإشارة المرجعية. لن تظهر فقرتها في جدول المحتويات كمدخل.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFigersLabel" الخاصة بجدول المحتويات ويقع ضمن حدود الإشارة المرجعية.
// يشير هذا الحقل أيضًا إلى إشارة مرجعية أخرى. ستظهر محتويات تلك الإشارة المرجعية في إدخال جدول المحتويات لحقل التسلسل هذا.
// لن يعرض حقل SEQ نفسه محتويات تلك الإشارة المرجعية.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// قم بإنشاء إشارة مرجعية بالمحتويات التي ستظهر في إدخال جدول المحتويات نظرًا لأن حقل SEQ أعلاه يشير إليها.
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

* class [FieldSeq](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
