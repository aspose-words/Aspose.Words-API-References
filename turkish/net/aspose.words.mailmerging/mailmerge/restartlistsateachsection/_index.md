---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: .NET için Aspose.Words
description: MailMerge RestartListsAtEachSection özelliğini keşfedin; sorunsuz posta birleştirmeleri için her bölümde kontrol listesi sıfırlanır. Belgenizin hassasiyetini bugün artırın!
type: docs
weight: 110
url: /tr/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Bir posta birleştirmenin yürütülmesinden sonra listelerin her bölümde yeniden başlatılıp başlatılmayacağını belirten bir değer alır veya ayarlar.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## Notlar

Varsayılan değer:`doğru` .

## Örnekler

Posta birleştirme işlemi gerçekleştirildiğinde liste numaralandırmasının her bölümde yeniden başlatılıp başlatılmayacağının nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
