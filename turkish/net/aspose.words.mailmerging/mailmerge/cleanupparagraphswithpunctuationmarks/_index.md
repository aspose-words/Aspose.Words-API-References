---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words for .NET API Referansı
description: MailMerge mülk. Noktalama işaretli paragrafların boş olarak kabul edilip edilmeyeceğini ve eğerRemoveEmptyParagraphs seçenek belirtildi.
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

Noktalama işaretli paragrafların boş olarak kabul edilip edilmeyeceğini ve eğerRemoveEmptyParagraphs seçenek belirtildi.

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

### Notlar

Varsayılan değer:`doğru` .

Temizlenebilir noktalama işaretlerinin tam listesi:

* !
* ,
* .
* :
* ;
* ?
* ¡
* ¿

### Örnekler

Adres-mektup birleştirme işleminden sonra noktalama işaretli paragrafların nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// Bu adres-mektup birleştirmenin oluşturacağı boş paragrafları kaldırmak için "CleanupOptions" özelliğini yapılandırın.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// "CleanupParagraphsWithPunctuationMarks" özelliğinin "true" olarak ayarlanması paragrafları da sayar
// noktalama işaretleri boş olarak kullanılır ve adres-mektup birleştirme işleminin bunları da kaldırmasını sağlar.
// "CleanupParagraphsWithPunctuationMarks" özelliğini "false" olarak ayarlama
// boş paragrafları kaldıracak, ancak noktalama işaretlerini kaldıracak.
// Bu, bu özelliğin ilgili olduğu noktalama işaretlerinin bir listesidir: "!", ",", ".", ":", ";", "?", "¡", "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)


