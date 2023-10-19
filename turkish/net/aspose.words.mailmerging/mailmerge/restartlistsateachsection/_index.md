---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words for .NET
description: MailMerge RestartListsAtEachSection mülk. Adresmektup birleştirme yürütüldükten sonra her bölümde listelerin yeniden başlatılıp başlatılmayacağını belirten bir değer alır veya ayarlar C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Adres-mektup birleştirme yürütüldükten sonra her bölümde listelerin yeniden başlatılıp başlatılmayacağını belirten bir değer alır veya ayarlar.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## Notlar

Varsayılan değer:`doğru` .

## Örnekler

Adres-mektup birleştirme gerçekleştirilirken her bölümde liste numaralandırmanın yeniden başlatılıp başlatılmayacağının nasıl denetleneceğini gösterir.

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
