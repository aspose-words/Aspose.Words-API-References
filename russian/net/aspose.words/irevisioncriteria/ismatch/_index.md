---
title: IRevisionCriteria.IsMatch
linktitle: IsMatch
articleTitle: IsMatch
second_title: Aspose.Words для .NET
description: Узнайте, как метод IRevisionCriteria IsMatch эффективно проверяет, соответствует ли конкретная ревизия вашим критериям для получения оптимальных результатов.
type: docs
weight: 10
url: /ru/net/aspose.words/irevisioncriteria/ismatch/
---
## IRevisionCriteria.IsMatch method

Проверяет, указано ли*revision* соответствует критериям.

```csharp
public bool IsMatch(Revision revision)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| revision | Revision | The[`Revision`](../../revision/) экземпляр для соответствия критериям. |

### Возвращаемое значение

`Истинный` если*revision* соответствует критериям, в противном случае`ЛОЖЬ`.

## Примечания

Реализация метода не должна принимать/отклонять ревизию или изменять ее каким-либо образом из-за непредвиденных результатов.

## Примеры

Показывает, как принять или отклонить изменение на основе критериев.

```csharp
public void RevisionSpecifiedCriteria()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Write("This does not count as a revision. ");

    // Чтобы зарегистрировать наши правки как ревизии, нам нужно объявить автора, а затем начать отслеживать их.
    doc.StartTrackRevisions("John Doe", DateTime.Now);
    builder.Write("This is insertion revision #1. ");
    doc.StopTrackRevisions();

    doc.StartTrackRevisions("Jane Doe", DateTime.Now);
    builder.Write("This is insertion revision #2. ");
    // Удалить запуск «Это не считается ревизией».
    doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();
    doc.StopTrackRevisions();

    Assert.AreEqual(3, doc.Revisions.Count);
    // У нас есть две редакции от разных авторов, поэтому нам нужно принять только одну.
    doc.Revisions.Accept(new RevisionCriteria("John Doe", RevisionType.Insertion));
    Assert.AreEqual(2, doc.Revisions.Count);
    // Отклонить ревизию с другим именем автора и типом ревизии.
    doc.Revisions.Reject(new RevisionCriteria("Jane Doe", RevisionType.Deletion));
    Assert.AreEqual(1, doc.Revisions.Count);

    doc.Save(ArtifactsDir + "Revision.RevisionSpecifiedCriteria.docx");
}

/// <summary>
/// Контролируйте, когда следует принять/отклонить определенную ревизию.
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

### Смотрите также

* class [Revision](../../revision/)
* interface [IRevisionCriteria](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
