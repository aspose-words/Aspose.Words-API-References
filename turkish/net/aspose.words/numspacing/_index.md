---
title: NumSpacing Enum
linktitle: NumSpacing
articleTitle: NumSpacing
second_title: .NET için Aspose.Words
description: Gelişmiş belge biçimlendirmesi için sayısal aralıkları özelleştirmek üzere Aspose.Words.NumSpacing enum'unu keşfedin. Metin sunumunuzu bugün yükseltin!
type: docs
weight: 5030
url: /tr/net/aspose.words/numspacing/
---
## NumSpacing enumeration

Sayısal aralıkların görüntülenebileceği olası değerleri belirtir.

```csharp
public enum NumSpacing
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Default | `0` | Rakamların yazı tipinin varsayılan biçiminde görüntüleneceğini belirtir. |
| Proportional | `1` | Yazı tipi tarafından destekleniyorsa, orantılı aralıklı olarak tasarlanan rakamların biçimlerinin görüntüleneceğini belirtir. |
| Tabular | `2` | Tablo olarak tasarlanan rakamların biçimlerinin, yazı tipi tarafından destekleniyorsa görüntüleneceğini belirtir. |

## Örnekler

Rakamların aralık türünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu efekt yalnızca MS Word'ün yeni sürümlerinde desteklenmektedir.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
