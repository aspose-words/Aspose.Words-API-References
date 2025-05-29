---
title: IRevisionCriteria.IsMatch
linktitle: IsMatch
articleTitle: IsMatch
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة IRevisionCriteria IsMatch بالتحقق بشكل فعال مما إذا كانت المراجعة المحددة تتوافق مع معاييرك لتحقيق أفضل النتائج.
type: docs
weight: 10
url: /ar/net/aspose.words/irevisioncriteria/ismatch/
---
## IRevisionCriteria.IsMatch method

يتحقق ما إذا كان محددًا أم لا*revision* يطابق المعايير.

```csharp
public bool IsMatch(Revision revision)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| revision | Revision | ال[`Revision`](../../revision/) مثال لمطابقة المعايير. |

### قيمة الإرجاع

`حقيقي` إذا كان*revision* يطابق المعايير، وإلا`خطأ شنيع`.

## ملاحظات

لا ينبغي لتطبيق الطريقة قبول/رفض المراجعة أو تعديلها بأي شكل من الأشكال بسبب نتائج غير متوقعة.

## أمثلة

يوضح كيفية قبول المراجعة أو رفضها استنادًا إلى المعايير.

```csharp
public void RevisionSpecifiedCriteria()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Write("This does not count as a revision. ");

    // لتسجيل تعديلاتنا كمراجعات، نحتاج إلى إعلان المؤلف، ثم البدء في تعقبها.
    doc.StartTrackRevisions("John Doe", DateTime.Now);
    builder.Write("This is insertion revision #1. ");
    doc.StopTrackRevisions();

    doc.StartTrackRevisions("Jane Doe", DateTime.Now);
    builder.Write("This is insertion revision #2. ");
    // قم بإزالة تشغيل "هذا لا يعد بمثابة مراجعة".
    doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();
    doc.StopTrackRevisions();

    Assert.AreEqual(3, doc.Revisions.Count);
    // لدينا مراجعتان من مؤلفين مختلفين، لذلك نحتاج إلى قبول واحدة فقط.
    doc.Revisions.Accept(new RevisionCriteria("John Doe", RevisionType.Insertion));
    Assert.AreEqual(2, doc.Revisions.Count);
    // رفض المراجعة التي تحمل اسم مؤلف مختلف ونوع مراجعة مختلف.
    doc.Revisions.Reject(new RevisionCriteria("Jane Doe", RevisionType.Deletion));
    Assert.AreEqual(1, doc.Revisions.Count);

    doc.Save(ArtifactsDir + "Revision.RevisionSpecifiedCriteria.docx");
}

/// <summary>
/// التحكم في متى يجب قبول أو رفض مراجعة معينة.
/// </summary>
public class RevisionCriteria : IRevisionCriteria
{
    private readonly string AuthorName;
    private readonly RevisionType RevisionType;

    public RevisionCriteria(string authorName, RevisionType revisionType)
    {
        AuthorName = authorName;
        RevisionType = revisionType;
    }

    public bool IsMatch(Revision revision)
    {
        return revision.Author == AuthorName && revision.RevisionType == RevisionType;
    }
}
```

### أنظر أيضا

* class [Revision](../../revision/)
* interface [IRevisionCriteria](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
