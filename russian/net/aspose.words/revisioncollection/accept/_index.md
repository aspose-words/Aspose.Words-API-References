---
title: RevisionCollection.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words для .NET
description: Откройте для себя метод RevisionCollection Accept, который позволяет легко управлять и фильтровать ревизии на основе ваших критериев для упрощения обновлений проекта.
type: docs
weight: 40
url: /ru/net/aspose.words/revisioncollection/accept/
---
## RevisionCollection.Accept method

Принимает изменения, соответствующие указанным критериям.

```csharp
public int Accept(IRevisionCriteria criteria)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| criteria | IRevisionCriteria | [`IRevisionCriteria`](../../irevisioncriteria/) реализация. |

### Возвращаемое значение

Количество принятых ревизий.

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

* interface [IRevisionCriteria](../../irevisioncriteria/)
* class [RevisionCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
