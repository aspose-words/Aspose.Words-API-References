---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
linktitle: CleanupParagraphsWithPunctuationMarks
articleTitle: CleanupParagraphsWithPunctuationMarks
second_title: .NET için Aspose.Words
description: MailMerge'inizi CleanupParagraphsWithPunctuationMarks özelliğiyle optimize edin. Daha temiz, profesyonel belgeler için boş paragraf kaldırmayı kontrol edin.
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

Noktalama işaretli paragrafların boş olarak kabul edilip edilmeyeceğini ve kaldırılıp kaldırılmayacağını belirten bir değer alır veya ayarlar.RemoveEmptyParagraphs seçenek belirtildi.

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

## Notlar

Varsayılan değer:`doğru` .

İşte temizlenebilir noktalama işaretlerinin tam listesi:

* !
* ,
* .
* :
* ;
* ?
* ¡
* ¿

## Örnekler

Bir posta birleştirme işleminden sonra noktalama işaretli paragrafların nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// Bu posta birleştirme işleminin oluşturacağı boş paragrafları kaldırmak için "CleanupOptions" özelliğini yapılandırın.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// "CleanupParagraphsWithPunctuationMarks" özelliğini "true" olarak ayarlamak paragrafları da sayacaktır
// noktalama işaretleri boş olarak eklenecek ve birleştirme işlemiyle bunların da kaldırılması sağlanacaktır.
// "CleanupParagraphsWithPunctuationMarks" özelliğini "false" olarak ayarlama
// boş paragrafları kaldıracak, ancak noktalama işaretli olanları kaldırmayacak.
// Bu özelliğin ilgilendiği noktalama işaretlerinin listesi şöyledir: "!", ",", ".", ":", ";", "?", "¡", "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
