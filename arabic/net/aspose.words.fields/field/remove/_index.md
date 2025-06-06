---
title: Field.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words لـ .NET
description: أزل الحقول من المستندات بسهولة باستخدام طريقة "إزالة الحقول". احصل على عوائد دقيقة للعقد، وتعامل مع الحقول الفارغة بسلاسة. حسّن سير عملك!
type: docs
weight: 120
url: /ar/net/aspose.words.fields/field/remove/
---
## Field.Remove method

يُزيل الحقل من المستند. يُرجع عقدة بعد الحقل مباشرةً. إذا كانت نهاية الحقل هي آخر عقدة فرعية للعقدة الأصلية، تُرجع فقرته الأصلية. إذا كان الحقل قد حُذف مُسبقًا، تُرجع`باطل` .

```csharp
public Node Remove()
```

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
// 1 - الحصول على حقل لإزالة نفسه:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - الحصول على المجموعة لإزالة الحقل الذي نمرره إلى طريقة الإزالة الخاصة به:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - إزالة حقل من مجموعة عند الفهرس:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - إزالة جميع الحقول من المجموعة مرة واحدة:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

يوضح كيفية معالجة الحقول الخاصة.

```csharp
public void FieldPrivate()
{
    // افتح مستند Corel WordPerfect الذي قمنا بتحويله إلى تنسيق .docx.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // قد تحتوي مستندات WordPerfect 5.x/6.x مثل تلك التي قمنا بتحميلها على حقول خاصة.
    // يحتفظ Microsoft Word بالحقول الخاصة أثناء عمليات التحميل/الحفظ،
    //ولكن لا يوفر أي وظيفة لهم.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    //يمكننا أيضًا إدراج الحقول الخاصة باستخدام منشئ المستندات.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    //هذه الحقول ليست طريقة فعالة لحماية المعلومات الحساسة.
    // ما لم يكن التوافق مع الإصدارات الأقدم من WordPerfect ضروريًا،
    // يمكننا إزالة هذه الحقول بأمان. يمكننا القيام بذلك باستخدام أداة DocumentVisiitor.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// يقوم بإزالة جميع الحقول الخاصة التي تم مواجهتها.
/// </summary>
public class FieldPrivateRemover : DocumentVisitor
{
    public FieldPrivateRemover()
    {
        mFieldsRemovedCount = 0;
    }

    public int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة FieldEnd في المستند.
    /// إذا كانت العقدة تنتمي إلى حقل خاص، فسيتم إزالة الحقل بأكمله.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.FieldType == FieldType.FieldPrivate)
        {
            fieldEnd.GetField().Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction.Continue;
    }

    private int mFieldsRemovedCount;
}
```

### أنظر أيضا

* class [Node](../../../aspose.words/node/)
* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
