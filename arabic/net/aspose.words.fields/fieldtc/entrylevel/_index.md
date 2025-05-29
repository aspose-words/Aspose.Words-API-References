---
title: FieldTC.EntryLevel
linktitle: EntryLevel
articleTitle: EntryLevel
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldTC EntryLevel، وقم بإدارة وتخصيص مستويات الدخول الخاصة بك بسهولة لتحسين الكفاءة وتبسيط سير العمل.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldtc/entrylevel/
---
## FieldTC.EntryLevel property

يحصل على مستوى الإدخال أو يعينه.

```csharp
public string EntryLevel { get; set; }
```

## أمثلة

يوضح كيفية إدراج حقل جدول المحتويات، وتصفية حقول جدول المحتويات التي تنتهي كإدخالات.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // قم بإدراج حقل جدول المحتويات، والذي سيقوم بتجميع كل حقول جدول المحتويات في جدول المحتويات.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // قم بتكوين الحقل فقط لالتقاط إدخالات TC من النوع "A"، ومستوى الإدخال بين 1 و3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    //سيظهر هذان الإدخالان في الجدول.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    //سيتم حذف هذا الإدخال من الجدول لأنه من نوع مختلف عن "A".
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // سيتم حذف هذا الإدخال من الجدول لأنه يحتوي على مستوى إدخال خارج النطاق 1-3.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// استخدم منشئ المستندات لإدراج حقل TC.
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### أنظر أيضا

* class [FieldTC](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
