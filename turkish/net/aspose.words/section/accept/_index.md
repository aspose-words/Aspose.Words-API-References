---
title: Section.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words for .NET
description: Section Accept yöntem. Ziyaretçi kabul eder C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words/section/accept/
---
## Section.Accept method

Ziyaretçi kabul eder.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| visitor | DocumentVisitor | Düğümleri ziyaret edecek ziyaretçi. |

### Geri dönüş değeri

Tüm düğümler ziyaret edilmişse doğrudur; yanlış ise[`DocumentVisitor`](../../documentvisitor/) tüm düğümleri ziyaret etmeden işlemi durdurdu.

## Notlar

Bu düğümü ve tüm alt öğelerini numaralandırır. Her düğüm kendisine karşılık gelen bir yöntemi çağırır.[`DocumentVisitor`](../../documentvisitor/).

Daha fazla bilgi için Ziyaretçi tasarım desenine bakın.

Çağrılar[`VisitSectionStart`](../../documentvisitor/visitsectionstart/) , ardından arar[`Accept`](../../node/accept/) bölümün tüm alt düğümleri için ve çağrılar[`VisitSectionEnd`](../../documentvisitor/visitsectionend/) sonunda.

### Ayrıca bakınız

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
