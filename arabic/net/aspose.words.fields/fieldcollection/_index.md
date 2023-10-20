---
title: FieldCollection Class
linktitle: FieldCollection
articleTitle: FieldCollection
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.FieldCollection فصل. مجموعة منField الكائنات التي تمثل الحقول في النطاق المحدد في C#.
type: docs
weight: 1690
url: /ar/net/aspose.words.fields/fieldcollection/
---
## FieldCollection class

مجموعة من[`Field`](../field/) الكائنات التي تمثل الحقول في النطاق المحدد.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldCollection : IEnumerable<Field>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.fields/fieldcollection/count/) { get; } | إرجاع عدد الحقول في المجموعة. |
| [Item](../../aspose.words.fields/fieldcollection/item/) { get; } | إرجاع حقل في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words.fields/fieldcollection/clear/)() | إزالة كافة حقول هذه المجموعة من المستند ومن هذه المجموعة نفسها. |
| [GetEnumerator](../../aspose.words.fields/fieldcollection/getenumerator/)() | يُرجع كائن العداد. |
| [Remove](../../aspose.words.fields/fieldcollection/remove/)(*[Field](../field/)*) | إزالة الحقل المحدد من هذه المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words.fields/fieldcollection/removeat/)(*int*) | إزالة حقل في الفهرس المحدد من هذه المجموعة ومن المستند. |

## ملاحظات

مثيل لهذه المجموعة يكرر الحقول التي تقع ضمن النطاق المحدد.

ال`FieldCollection` لا تمتلك المجموعة الحقول التي تحتوي عليها، بل هي مجرد مجموعة مختارة من الحقول.

ال`FieldCollection` المجموعة "مباشرة"، أي أن التغييرات التي يتم إجراؤها على العناصر الفرعية للعقدة object التي تم إنشاؤها منها تنعكس فورًا في الحقول التي يتم إرجاعها بواسطة`FieldCollection` الخصائص والأساليب.

## أمثلة

يوضح كيفية إزالة الحقول من مجموعة الحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// فيما يلي أربع طرق لإزالة الحقول من مجموعة الحقول.
// 1 - احصل على حقل لإزالة نفسه:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - احصل على المجموعة لإزالة الحقل الذي نمرره إلى طريقة الإزالة الخاصة به:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - إزالة حقل من مجموعة في فهرس:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - قم بإزالة كافة الحقول من المجموعة مرة واحدة:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

يوضح كيفية العمل مع مجموعة من الحقول.

```csharp
public void FieldCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // كرر المجموعة الميدانية واطبع المحتويات واكتبها
    // لكل حقل باستخدام تطبيق زائر مخصص.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());
}

/// <summary>
/// تنفيذ مستند الزائر الذي يطبع معلومات الحقل.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// يحصل على النص العادي للمستند الذي قام الزائر بتجميعه.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة FieldStart في المستند.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة FieldSeparator في المستند.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة FieldEnd في المستند.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
