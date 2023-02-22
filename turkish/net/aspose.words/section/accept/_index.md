---
title: Section.Accept
second_title: Aspose.Words for .NET API Referansı
description: Section yöntem. Bir ziyaretçiyi kabul eder.
type: docs
weight: 70
url: /tr/net/aspose.words/section/accept/
---
## Section.Accept method

Bir ziyaretçiyi kabul eder.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| visitor | DocumentVisitor | Düğümleri ziyaret edecek ziyaretçi. |

### Geri dönüş değeri

Tüm düğümler ziyaret edildiyse doğrudur; DocumentVisitor tüm düğümleri ziyaret etmeden önce işlemi durdurduysa false.

### Notlar

Bu düğüm ve tüm alt öğeleri üzerinde numaralandırır. Her düğüm, DocumentVisitor'da karşılık gelen bir yöntemi çağırır.

Daha fazla bilgi için Ziyaretçi tasarım modeline bakın.

DocumentVisitor.VisitSectionStart'ı çağırır, ardından bölüm 'nin tüm alt düğümleri için Kabul Et'i çağırır ve sonunda DocumentVisitor.VisitSectionEnd'i çağırır.

### Ayrıca bakınız

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* ad alanı [Aspose.Words](../../section/)
* toplantı [Aspose.Words](../../../)


