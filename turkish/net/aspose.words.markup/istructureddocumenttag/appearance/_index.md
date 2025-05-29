---
title: IStructuredDocumentTag.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: .NET için Aspose.Words
description: Kullanıcı deneyimini iyileştirmek için yapılandırılmış belge etiketlerinizi özelleştirmek ve geliştirmek amacıyla IStructuredDocumentTag Görünüm özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.markup/istructureddocumenttag/appearance/
---
## IStructuredDocumentTag.Appearance property

Yapılandırılmış belge etiketinin görünümünü alır veya ayarlar.

```csharp
public SdtAppearance Appearance { get; set; }
```

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

* enum [SdtAppearance](../../sdtappearance/)
* interface [IStructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
