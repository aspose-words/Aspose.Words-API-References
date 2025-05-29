---
title: RevisionCollection.Accept
linktitle: Accept
articleTitle: Accept
second_title: .NET için Aspose.Words
description: Proje güncellemelerinin daha kolay ve hızlı olması için kriterlerinize göre revizyonları kolayca yönetmek ve filtrelemek amacıyla RevisionCollection Accept yöntemini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words/revisioncollection/accept/
---
## RevisionCollection.Accept method

Belirtilen ölçütlerle eşleşen revizyonları kabul eder.

```csharp
public int Accept(IRevisionCriteria criteria)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| criteria | IRevisionCriteria | [`IRevisionCriteria`](../../irevisioncriteria/) uygulama. |

### Geri dönüş değeri

Kabul edilen revizyonların sayısı.

## Örnekler

Kriterlere göre revizyonun nasıl kabul edileceğini veya reddedileceğini gösterir.

```csharp
public void RevisionSpecifiedCriteria()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Write("This does not count as a revision. ");

    // Düzenlemelerimizi revizyon olarak kaydetmek için bir yazar bildirmemiz ve ardından bunları izlemeye başlamamız gerekiyor.
    doc.StartTrackRevisions("John Doe", DateTime.Now);
    builder.Write("This is insertion revision #1. ");
    doc.StopTrackRevisions();

    doc.StartTrackRevisions("Jane Doe", DateTime.Now);
    builder.Write("This is insertion revision #2. ");
    // "Bu bir revizyon olarak sayılmaz." çalıştırmasını kaldır.
    doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();
    doc.StopTrackRevisions();

    Assert.AreEqual(3, doc.Revisions.Count);
    // Farklı yazarlardan iki revizyonumuz var, bu yüzden yalnızca birini kabul etmemiz gerekiyor.
    doc.Revisions.Accept(new RevisionCriteria("John Doe", RevisionType.Insertion));
    Assert.AreEqual(2, doc.Revisions.Count);
    // Farklı yazar adı ve revizyon türüyle yapılan revizyonu reddedin.
    doc.Revisions.Reject(new RevisionCriteria("Jane Doe", RevisionType.Deletion));
    Assert.AreEqual(1, doc.Revisions.Count);

    doc.Save(ArtifactsDir + "Revision.RevisionSpecifiedCriteria.docx");
}

/// <summary>
/// Belirli bir revizyonun ne zaman kabul edileceğini/reddedileceğini kontrol edin.
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

### Ayrıca bakınız

* interface [IRevisionCriteria](../../irevisioncriteria/)
* class [RevisionCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
