---
title: SdtAppearance Enum
linktitle: SdtAppearance
articleTitle: SdtAppearance
second_title: .NET için Aspose.Words
description: Yapılandırılmış belge etiketi görünümlerini özelleştirmek için Aspose.Words.Markup.SdtAppearance enum'unu keşfedin. Belge biçimlendirmenizi zahmetsizce geliştirin!
type: docs
weight: 4680
url: /tr/net/aspose.words.markup/sdtappearance/
---
## SdtAppearance enumeration

Yapılandırılmış bir belge etiketinin görünümünü belirtir.

```csharp
public enum SdtAppearance
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| BoundingBox | `0` | Gölgeli bir dikdörtgen veya sınırlayıcı kutu olarak gösterilen yapılandırılmış bir belge etiketini temsil eder. |
| Tags | `1` | Başlangıç ve bitiş işaretçileri olarak gösterilen yapılandırılmış bir belge etiketini temsil eder. |
| Hidden | `2` | Gösterilmeyen yapılandırılmış bir belge etiketini temsil eder. |
| Default | `0` | Varsayılan olarakBoundingBox . |

## Örnekler

İçeriğin etrafında etiketin nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
