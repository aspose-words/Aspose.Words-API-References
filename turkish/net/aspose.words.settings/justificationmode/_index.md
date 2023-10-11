---
title: Enum JustificationMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Settings.JustificationMode Sıralama. Bir belge için karakter aralığı ayarını belirtir. Varsayılan değerGenişletmek .
type: docs
weight: 5800
url: /tr/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Bir belge için karakter aralığı ayarını belirtir. Varsayılan değer:`Genişletmek` .

```csharp
public enum JustificationMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Expand | `0` |  |
| Compress | `1` |  |
| CompressKana | `2` |  |

### Örnekler

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


