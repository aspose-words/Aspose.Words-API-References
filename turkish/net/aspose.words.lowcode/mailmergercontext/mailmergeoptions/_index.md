---
title: MailMergerContext.MailMergeOptions
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: .NET için Aspose.Words
description: Belge otomasyonunuzu kolaylaştırmak ve iş akışı verimliliğinizi zahmetsizce artırmak için MailMergeContext MailMergeOptions özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.lowcode/mailmergercontext/mailmergeoptions/
---
## MailMergerContext.MailMergeOptions property

Posta birleştirme seçenekleri.

```csharp
public MailMergeOptions MailMergeOptions { get; }
```

## Örnekler

Bağlam kullanılarak tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContext.docx")
    .Execute();
```

Akıştaki tek bir kayıt için bağlam kullanılarak posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak posta birleştirme işlemini yapmanın birkaç yolu vardır:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Ayrıca bakınız

* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMergerContext](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
