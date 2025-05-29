---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: .NET için Aspose.Words
description: OOXML belgelerinizin uyumluluk standartlarını zahmetsizce karşıladığından emin olun. Aracımız, OOXML uyumluluğunu doğrulamak için içeriği analiz ederek belge bütünlüğünü artırır.
type: docs
weight: 70
url: /tr/net/aspose.words/document/compliance/
---
## Document.Compliance property

Yüklenen belge içeriğinden belirlenen OOXML uyumluluk sürümünü alır. Yalnızca OOXML belgeleri için mantıklıdır.

```csharp
public OoxmlCompliance Compliance { get; }
```

## Notlar

Yeni boş bir belge oluşturduysanız veya OOXML olmayan bir belge yüklediyseniz document şunu döndürür:Ecma376_2006 değer.

## Örnekler

Yüklenen bir belgenin Open Office XML uyumlu sürümünün nasıl okunacağını gösterir.

```csharp
// Uyumluluk sürümü, Microsoft Word'ün farklı sürümleriyle oluşturulan belgelere göre değişir.
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
