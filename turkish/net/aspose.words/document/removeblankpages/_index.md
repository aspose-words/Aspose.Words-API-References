---
title: Document.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: .NET için Aspose.Words
description: RemoveBlankPages yöntemiyle belgelerinizi zahmetsizce geliştirin; istenmeyen boş sayfaları ortadan kaldırarak cilalı, profesyonel bir görünüm elde edin.
type: docs
weight: 700
url: /tr/net/aspose.words/document/removeblankpages/
---
## Document.RemoveBlankPages method

Belgeden boş sayfaları kaldırır.

```csharp
public List<int> RemoveBlankPages()
```

### Geri dönüş değeri

Sayfa numaraları listesi boş kabul edilerek kaldırılmıştır.

## Notlar

Ortaya çıkan belge, numaralandırma, üstbilgiler/altbilgiler ve genel düzen dahil olmak üzere diğer içerikler, değişmeden kalırken boş kabul edilen sayfaları içermeyecektir. Sayfanın gövdesinde görünür içerik olmadığında sayfa boş kabul edilir, örneğin, kenarlığı olmayan boş bir tablo görünmez olarak kabul edilecek ve bu nedenle sayfa boş olarak algılanacaktır.

## Örnekler

Belgeden boş sayfaların nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Blank pages.docx");
Assert.AreEqual(2, doc.PageCount);
doc.RemoveBlankPages();
doc.UpdatePageLayout();
Assert.AreEqual(1, doc.PageCount);
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
