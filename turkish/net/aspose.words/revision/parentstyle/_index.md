---
title: Revision.ParentStyle
linktitle: ParentStyle
articleTitle: ParentStyle
second_title: .NET için Aspose.Words
description: StyleDefinitionChange revizyonları için doğrudan üst stil sahibini tanımlayan Revision ParentStyle özelliğini keşfedin. Stil oluşturma sürecinizi optimize edin!
type: docs
weight: 50
url: /tr/net/aspose.words/revision/parentstyle/
---
## Revision.ParentStyle property

Bu revizyonun doğrudan üst stilini (sahibini) alır. Bu özellik yalnızca şu sürüm için çalışacaktır:StyleDefinitionChange revizyon türü.

```csharp
public Style ParentStyle { get; }
```

## Notlar

Bu revizyon belge düğümlerindeki değişikliklerle ilgiliyse, şunu kullanın:[`ParentNode`](../parentnode/) bunun yerine.

## Örnekler

Bir belgenin revizyon koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Bu koleksiyonun kendisi de bir revizyon grupları koleksiyonuna sahiptir.
// Her grup, bitişik revizyonların bir dizisidir.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Grup koleksiyonu üzerinde yineleme yap ve revizyonun ilgilendiği metni yazdır.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Bir revizyonun etkilediği her Çalıştırma, karşılık gelen bir Revizyon nesnesi alır.
// Revizyonların koleksiyonu yukarıda bastığımız yoğunlaştırılmış formdan önemli ölçüde daha büyüktür,
// Microsoft Word düzenlemesi sırasında belgeyi kaç Çalıştırmaya böldüğümüze bağlı olarak.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // Bir StyleDefinitionChange kesinlikle stilleri etkiler ve belge düğümlerini etkilemez. Bu, "ParentStyle" anlamına gelir
        // özellik her zaman kullanımda olacak, ParentNode ise her zaman null olacaktır.
        // Diğer tüm değişiklikler düğümleri etkilediğinden, ParentNode kullanımda olacak ve ParentStyle boş olacaktır.
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

// Koleksiyon üzerinden yapılan tüm düzeltmeleri reddederek belgeyi orijinal haline geri döndür.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Ayrıca bakınız

* class [Style](../../style/)
* class [Revision](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
