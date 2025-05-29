---
title: RevisionColor Enum
linktitle: RevisionColor
articleTitle: RevisionColor
second_title: .NET için Aspose.Words
description: Belge revizyon renklerini özelleştirmek, netliği artırmak ve belgelerinizdeki iş birliğini geliştirmek için Aspose.Words.Layout.RevisionColor enum'unu keşfedin.
type: docs
weight: 3830
url: /tr/net/aspose.words.layout/revisioncolor/
---
## RevisionColor enumeration

Belge revizyonlarının rengini belirtmeye izin verir.

```csharp
public enum RevisionColor
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `0` | Varsayılan. |
| Black | `1` | 000000 rengini temsil eder. |
| Blue | `2` | 2e97d3 rengini temsil eder. |
| BrightGreen | `3` | 84a35b rengini temsil eder. |
| ClassicBlue | `4` | 0000ff rengini temsil eder. |
| ClassicRed | `5` | ff0000 rengini temsil eder. |
| DarkBlue | `6` | 376e96 rengini temsil eder. |
| DarkRed | `7` | 881824 rengini temsil eder. |
| DarkYellow | `8` | e09a2b rengini temsil eder. |
| Gray25 | `9` | a0a3a9 rengini temsil eder. |
| Gray50 | `10` | 50565e rengini temsil eder. |
| Green | `11` | 2c6234 rengini temsil eder. |
| Pink | `12` | ce338f rengini temsil eder. |
| Red | `13` | b5082e rengini temsil eder. |
| Teal | `14` | 1b9cab rengini temsil eder. |
| Turquoise | `15` | 3eafc2 rengini temsil eder. |
| Violet | `16` | 633277 rengini temsil eder. |
| White | `17` | ffffff rengini temsil eder. |
| Yellow | `18` | fad272 rengini temsil eder. |
| LightPink | `19` | fce6f4 rengini temsil eder. |
| LightBlue | `20` | e1f2fa rengini temsil eder. |
| LightYellow | `21` | fef4de rengini temsil eder. |
| LightPurple | `22` | eadfef rengini temsil eder. |
| LightOrange | `23` | fce3d0 rengini temsil eder. |
| LightGreen | `24` | e9f8ce rengini temsil eder. |
| Gray | `25` | Efeded rengi temsil eder. |
| NoHighlight | `26` | Revizyon değişikliklerini vurgulamak için hiçbir renk kullanılmaz. |
| ByAuthor | `27` | Her yazarın revizyonları, önceden tanımlanmış bir dizi yüksek kontrastlı renk arasından vurgulanmak üzere kendi rengini alır. |

## Örnekler

İşlenmiş bir çıktı belgesindeki revizyonların görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir revizyon ekle, ardından tüm revizyonların rengini yeşil yap.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Her düzeltilen satırın solunda görünen çubuğu kaldır.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)
