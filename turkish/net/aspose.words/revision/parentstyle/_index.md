---
title: Revision.ParentStyle
linktitle: ParentStyle
articleTitle: ParentStyle
second_title: Aspose.Words for .NET
description: Revision ParentStyle mülk. Bu revizyonun doğrudan ana stilini sahibini alır. Bu özellik yalnızcaStyleDefinitionChange revizyon tipi C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words/revision/parentstyle/
---
## Revision.ParentStyle property

Bu revizyonun doğrudan ana stilini (sahibini) alır. Bu özellik yalnızcaStyleDefinitionChange revizyon tipi.

```csharp
public Style ParentStyle { get; }
```

## Notlar

Bu revizyon belge düğümlerindeki değişikliklerle ilgiliyse şunu kullanın:[`ParentNode`](../parentnode/) bunun yerine.

## Örnekler

Bir belgenin düzeltme koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Bu koleksiyonun kendisi revizyon gruplarından oluşan bir koleksiyona sahiptir.
// Her grup bitişik revizyonların bir dizisidir.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Grup koleksiyonu üzerinde yineleme yapın ve revizyonun ilgili olduğu metni yazdırın.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Bir revizyonun etkilediği her Çalıştırma, karşılık gelen bir Revizyon nesnesini alır.
// Revizyonların koleksiyonu yukarıda yazdırdığımız özet formdan oldukça daha büyüktür,
// Microsoft Word düzenleme sırasında belgeyi kaç Çalıştırmaya böldüğümüze bağlı.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // StyleDefinitionChange, belge düğümlerini değil, stilleri kesinlikle etkiler. Bu "Ebeveyn Stili" anlamına gelir
        // özellik her zaman kullanımda olacak, ParentNode ise her zaman boş olacaktır.
        // Diğer tüm değişiklikler düğümleri etkilediğinden, ParentNode tam tersi şekilde kullanımda olacak ve ParentStyle null olacaktır.
        if (e.Current.RevisionType == RevisionType.StyleDefinitionChange)
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, style: [{e.Current.ParentStyle.Name}]");
        }
        else
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, contents: [{e.Current.ParentNode.GetText().Trim()}]");
        }
    }
}

// Belgeyi orijinal formuna döndürerek koleksiyon aracılığıyla yapılan tüm düzeltmeleri reddedin.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Ayrıca bakınız

* class [Style](../../style/)
* class [Revision](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
