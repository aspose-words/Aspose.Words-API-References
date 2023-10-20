---
title: FieldRef.IncludeNoteOrComment
linktitle: IncludeNoteOrComment
articleTitle: IncludeNoteOrComment
second_title: Aspose.Words لـ .NET
description: FieldRef IncludeNoteOrComment ملكية. الحصول على أو تعيين ما إذا كان سيتم زيادة أرقام الحواشي السفلية والتعليقات الختامية والتعليقات التوضيحية التي تم وضع علامة عليها بواسطة الإشارة المرجعية وإدراج الحاشية السفلية والتعليقات الختامية ونص التعليق المقابل في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldref/includenoteorcomment/
---
## FieldRef.IncludeNoteOrComment property

الحصول على أو تعيين ما إذا كان سيتم زيادة أرقام الحواشي السفلية والتعليقات الختامية والتعليقات التوضيحية التي تم وضع علامة عليها بواسطة الإشارة المرجعية، وإدراج الحاشية السفلية والتعليقات الختامية ونص التعليق المقابل.

```csharp
public bool IncludeNoteOrComment { get; set; }
```

## أمثلة

يوضح كيفية إدراج حقول REF للإشارة إلى الإشارات المرجعية.

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // سوف نقوم بتطبيق تنسيق قائمة مخصص، حيث يشير مقدار الأقواس الزاوية إلى مستوى القائمة الذي نحن فيه حاليًا.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // أدخل حقل REF الذي سيحتوي على النص الموجود داخل الإشارة المرجعية الخاصة بنا، وسيكون بمثابة رابط تشعبي، واستنساخ الحواشي السفلية للإشارة المرجعية.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // أدخل حقل REF، واعرض ما إذا كانت الإشارة المرجعية أعلى أو أسفل منه.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // اعرض رقم قائمة الإشارة المرجعية كما يظهر في المستند.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // عرض رقم قائمة الإشارة المرجعية، ولكن مع حذف الأحرف غير المحددة، مثل الأقواس الزاوية.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // تحرك لأسفل مستوى القائمة بمقدار مستوى واحد.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // عرض رقم قائمة الإشارة المرجعية وأرقام جميع مستويات القائمة فوقها.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // عرض أرقام مستوى القائمة بين حقل REF هذا والإشارة المرجعية التي يشير إليها.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // في نهاية المستند، ستظهر الإشارة المرجعية كعنصر قائمة هنا.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// اطلب من منشئ المستندات إدراج حقل REF، والإشارة إلى إشارة مرجعية به، وإضافة نص قبله وبعده.
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### أنظر أيضا

* class [FieldRef](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
