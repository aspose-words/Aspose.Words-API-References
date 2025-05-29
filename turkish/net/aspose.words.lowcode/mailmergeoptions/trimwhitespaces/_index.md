---
title: MailMergeOptions.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: .NET için Aspose.Words
description: TrimWhitespaces özelliğiyle posta birleştirmenizi optimize edin. Daha temiz, daha profesyonel belgeler için öndeki ve arkadaki boşlukları kolayca yönetin.
type: docs
weight: 110
url: /tr/net/aspose.words.lowcode/mailmergeoptions/trimwhitespaces/
---
## MailMergeOptions.TrimWhitespaces property

Posta birleştirme değerlerinden son ve öndeki boşlukların kesilip kesilmeyeceğini belirten bir değer alır veya ayarlar.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Notlar

Varsayılan değer:`doğru` .

## Örnekler

Tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Posta birleştirme işlemini yapmanın birkaç yolu vardır:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Ayrıca bakınız

* class [MailMergeOptions](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
