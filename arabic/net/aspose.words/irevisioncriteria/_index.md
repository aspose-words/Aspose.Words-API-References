---
title: IRevisionCriteria Interface
linktitle: IRevisionCriteria
articleTitle: IRevisionCriteria
second_title: Aspose.Words لـ .NET
description: تحكم في مراجعات المستندات بسهولة مع Aspose.Words.IRevisionCriteria. خصّص قبول ورفض التغييرات لإدارة مستندات دقيقة.
type: docs
weight: 3650
url: /ar/net/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface

قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في وقت حدوث بعض[`Revision`](../revision/) يجب أن يتم قبولها/رفضها أو لا بواسطة[`Accept`](../revisioncollection/accept/)/[`Reject`](../revisioncollection/reject/) الأساليب.

```csharp
public interface IRevisionCriteria
```

## طُرق

| اسم | وصف |
| --- | --- |
| [IsMatch](../../aspose.words/irevisioncriteria/ismatch/)(*[Revision](../revision/)*) | يتحقق ما إذا كان محددًا أم لا*revision* يطابق المعايير. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
