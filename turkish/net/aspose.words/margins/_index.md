---
title: Margins Enum
linktitle: Margins
articleTitle: Margins
second_title: .NET için Aspose.Words
description: Özelleştirilebilir belge kenar boşlukları için Aspose.Words.Margins numaralandırmasını keşfedin. Kullanımı kolay ön ayarlarla belge biçimlendirmenizi geliştirin!
type: docs
weight: 4580
url: /tr/net/aspose.words/margins/
---
## Margins enumeration

Önceden ayarlanmış kenar boşluklarını belirtir.

```csharp
public enum Margins
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Normal | `0` | Normal kenar boşlukları. |
| Narrow | `1` | Dar kenar boşlukları. |
| Moderate | `2` | Orta düzeyde marjlar. |
| Wide | `3` | Geniş kenar boşlukları. |
| Mirrored | `4` | Yansıtılmış kenar boşlukları. |
| Custom | `5` | Özel kenar boşlukları. |

## Örnekler

Belgenin sayfa düzeninin ne zaman yeniden hesaplanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi PDF'e, görüntüye kaydetmek veya ilk kez yazdırmak otomatik olarak
// Belgenin düzenini sayfalarının içinde önbelleğe al.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Belgeyi bir şekilde değiştirin.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// Aspose.Words'ün geçerli sürümünde, belgeyi değiştirmek otomatik olarak yeniden oluşturmaz
// önbelleğe alınmış sayfa düzeni. Önbelleğe alınmış düzeni istiyorsak
// Güncel kalmak için manuel olarak güncellememiz gerekecek.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
