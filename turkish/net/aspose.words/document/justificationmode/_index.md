---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: .NET için Aspose.Words
description: JustificationMode özelliğiyle belgenizin karakter aralığını nasıl optimize edeceğinizi keşfedin. Okunabilirliği artırın ve sunumu zahmetsizce iyileştirin!
type: docs
weight: 240
url: /tr/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Bir belgenin karakter aralığı ayarını alır veya ayarlar.

```csharp
public JustificationMode JustificationMode { get; set; }
```

## Örnekler

Karakter aralığı kontrolünün nasıl yönetileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Ayrıca bakınız

* enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
