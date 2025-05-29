---
title: StructuredDocumentTagRangeStart.Accept
linktitle: Accept
articleTitle: Accept
second_title: .NET için Aspose.Words
description: StructuredDocumentTagRangeStart Accept yönteminin, sorunsuz entegrasyon için ziyaretçileri etkili bir şekilde kabul ederek belge işlemeyi nasıl geliştirdiğini keşfedin.
type: docs
weight: 200
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/accept/
---
## StructuredDocumentTagRangeStart.Accept method

Bir ziyaretçiyi kabul eder.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| visitor | DocumentVisitor | Düğümleri ziyaret edecek ziyaretçi. |

### Geri dönüş değeri

Tüm düğümler ziyaret edildiyse doğru; eğer ziyaret edilmediyse yanlış[`DocumentVisitor`](../../../aspose.words/documentvisitor/) tüm düğümleri ziyaret etmeden önce işlemi durdurdu.

## Notlar

Bu düğüm ve tüm alt düğümleri üzerinde numaralandırma yapar. Her düğüm, ilgili bir yöntemi çağırır[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Daha fazla bilgi için Ziyaretçi tasarım desenine bakın.

### Ayrıca bakınız

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeStart](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
