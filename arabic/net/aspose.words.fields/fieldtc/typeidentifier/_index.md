---
title: FieldTC.TypeIdentifier
second_title: Aspose.Words لمراجع .NET API
description: FieldTC ملكية. الحصول على أو تحديد معرف نوع لهذا الحقل والذي يكون عادةً حرفًا .
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldtc/typeidentifier/
---
## FieldTC.TypeIdentifier property

الحصول على أو تحديد معرف نوع لهذا الحقل (والذي يكون عادةً حرفًا) .

```csharp
public string TypeIdentifier { get; set; }
```

### أمثلة

يوضح كيفية إدراج حقل جدول المحتويات ، وتصفية حقول TC التي ينتهي بها المطاف كمدخلات.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل حقل جدول المحتويات ، والذي سيجمع جميع حقول TC في جدول محتويات.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // تكوين الحقل فقط لالتقاط مدخلات TC من النوع "A" ، ومستوى الإدخال بين 1 و 3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // سيظهر هذان المدخلان في الجدول.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // سيتم حذف هذا الإدخال من الجدول لأنه يحتوي على نوع مختلف عن "أ".
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // سيتم حذف هذا الإدخال من الجدول لأنه يحتوي على مستوى دخول خارج النطاق 1-3.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");

/// <summary>
/// استخدم أداة إنشاء المستندات لإدراج حقل TC.
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldtc/)
* المجسم [Aspose.Words](../../../)


