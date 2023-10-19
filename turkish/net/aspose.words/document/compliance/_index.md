---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words for .NET
description: Document Compliance mülk. Yüklenen belge içeriğinden belirlenen OOXML uyumluluk sürümünü alır. Yalnızca OOXML belgeleri için anlamlıdır C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words/document/compliance/
---
## Document.Compliance property

Yüklenen belge içeriğinden belirlenen OOXML uyumluluk sürümünü alır. Yalnızca OOXML belgeleri için anlamlıdır.

```csharp
public OoxmlCompliance Compliance { get; }
```

## Notlar

Yeni bir boş belge oluşturduysanız veya OOXML olmayan bir belge yüklediyseniz document şunu döndürür:Ecma376_2006 değer.

## Örnekler

Yüklenen bir belgenin Open Office XML uyumluluk sürümünün nasıl okunacağını gösterir.

```csharp
// Uyumluluk sürümü, Microsoft Word'ün farklı sürümleri tarafından oluşturulan belgeler arasında farklılık gösterir.
Document doc = new Document(MyDir + "Document.doc");

Assert.AreEqual(doc.Compliance, OoxmlCompliance.Ecma376_2006);

doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(doc.Compliance, OoxmlCompliance.Iso29500_2008_Transitional);
```

### Ayrıca bakınız

* enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
