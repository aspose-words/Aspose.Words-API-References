---
title: RevisionGroup.Text
linktitle: Text
articleTitle: Text
second_title: .NET için Aspose.Words
description: Eklenen, silinen veya taşınan metne erişmek için RevisionGroup Text özelliğini keşfedin; böylece belgenizin biçimlendirme içgörülerini ve düzenleme verimliliğini artırın.
type: docs
weight: 30
url: /tr/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

Eklenen/silinmiş/taşınan metni veya biçim değişikliğinin açıklamasını döndürür.

```csharp
public string Text { get; }
```

## Örnekler

Bir belgedeki revizyon grubuyla ilgili bilgilerin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### Ayrıca bakınız

* class [RevisionGroup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
