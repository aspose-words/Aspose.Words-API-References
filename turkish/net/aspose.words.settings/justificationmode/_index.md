---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: .NET için Aspose.Words
description: Belgelerinizde hassas karakter aralığı ayarlamaları için Aspose.Words JustificationMode enum'unu keşfedin. Özelleştirilebilir ayarlarla okunabilirliği artırın!
type: docs
weight: 6630
url: /tr/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Bir belge için karakter aralığı ayarlamasını belirtir. Varsayılan değer`Genişletmek` .

```csharp
public enum JustificationMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Expand | `0` | Karakter aralığını sıkıştırmayın. |
| Compress | `1` | Karakter aralığını sıkıştır. |
| CompressKana | `2` | Kana hecelerinin, Hiragana ve Katakana kurallarını kullanarak sıkıştırın. |

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

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
