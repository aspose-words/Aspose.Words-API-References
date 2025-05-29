---
title: FieldSeq.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldSeq BookmarkName لإدارة التنقل في المستندات بسهولة. عيّن أو استرجاع أسماء الإشارات المرجعية لسهولة الرجوع إلى العناصر.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

يحصل على اسم إشارة مرجعية أو يعينه بحيث يشير إلى عنصر في مكان آخر في المستند بدلاً من الموقع الحالي.

```csharp
public string BookmarkName { get; set; }
```

## أمثلة

يوضح كيفية دمج جدول المحتويات وحقول التسلسل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكن لحقل جدول المحتويات إنشاء إدخال في جدول المحتويات الخاص به لكل حقل تسلسل موجود في المستند.
// يحتوي كل إدخال على الفقرة التي تحتوي على حقل التسلسل،
// ورقم الصفحة التي يظهر فيها الحقل.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// قم بتكوين حقل جدول المحتويات هذا ليحتوي على خاصية SequenceIdentifier بقيمة "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// قم بتكوين حقل جدول المحتويات هذا لالتقاط حقول التسلسل فقط التي تقع ضمن حدود الإشارة المرجعية
// اسمه "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// تعرض حقول SEQ عددًا يتزايد عند كل حقل SEQ.
// تحتفظ هذه الحقول أيضًا بعدد منفصل لكل تسلسل مسمى فريد
// تم تحديده بواسطة خاصية "SequenceIdentifier" في حقل SEQ.
// أدخل حقل SEQ الذي يحتوي على معرف تسلسل يتطابق مع جدول المحتويات
// خاصية TableOfFiguresLabel. لن يُنشئ هذا الحقل إدخالاً في جدول المحتويات لأنه خارج
// حدود الإشارة المرجعية المحددة بواسطة "BookmarkName".
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

// لا يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFiguresLabel" في جدول المحتويات،
// ويقع ضمن حدود الإشارة المرجعية. لن تظهر فقرته في جدول المحتويات كمدخل.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// يتطابق تسلسل حقل SEQ هذا مع خاصية "TableOfFiguresLabel" في جدول المحتويات ويقع ضمن حدود الإشارة المرجعية.
// يشير هذا الحقل أيضًا إلى إشارة مرجعية أخرى. سيظهر محتوى هذه الإشارة المرجعية في مُدخل جدول المحتويات لحقل التسلسل هذا.
// لن يعرض حقل SEQ نفسه محتويات تلك الإشارة المرجعية.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// قم بإنشاء إشارة مرجعية بالمحتويات التي ستظهر في إدخال جدول المحتويات بسبب وجود حقل SEQ أعلاه يشير إليه.
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
