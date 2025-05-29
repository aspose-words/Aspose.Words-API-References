---
title: WarningSource Enum
linktitle: WarningSource
articleTitle: WarningSource
second_title: .NET için Aspose.Words
description: Gelişmiş belge yönetimi için belge yükleme ve kaydetme sırasında uyarı kaynaklarını tanımlayan Aspose.Words.WarningSource enum'unu keşfedin.
type: docs
weight: 7500
url: /tr/net/aspose.words/warningsource/
---
## WarningSource enumeration

Belge yükleme veya kaydetme sırasında uyarı üreten modülü belirtir.

```csharp
public enum WarningSource
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Unknown | `0` | Uyarı kaynağı belirtilmemiş. |
| Layout | `1` | Belge düzeni oluşturan modül. |
| DrawingML | `2` | DrawingML şekillerini oluşturan modül. |
| OfficeMath | `3` | OfficeMath'i oluşturan modül. |
| Shapes | `4` | Sıradan şekilleri oluşturan modül. |
| Metafile | `5` | Meta dosyalarını işleyen modül. |
| Xps | `6` | XPS'i oluşturan modül. |
| Pdf | `7` | PDF'yi işleyen modül. |
| Image | `8` | Görüntüleri işleyen modül. |
| Docx | `9` | DOCX dosyalarını okuyan/yazabilen modül. |
| Doc | `10` | İkili DOC dosyalarını okuyan/yazabilen modül. |
| Text | `11` | Düz metin dosyalarını okuyan/yazabilen modül. |
| Rtf | `12` | RTF dosyalarını okuyan/yazabilen modül. |
| WordML | `13` | WML dosyalarını okuyan/yazabilen modül. |
| Nrx | `14` | DOCX/WML okuyucu/yazıcı modülleri arasında paylaşılan ortak modüller. |
| Odt | `15` | ODT dosyalarını okuyan/yazabilen modül. |
| Html | `16` | HTML/MHTML dosyalarını okuyan/yazabilen modül. |
| Validator | `17` | Model tutarlılığını ve geçerliliğini doğrulayan modül. |
| Xaml | `18` | Xaml dosyalarını okuyan/yazabilen modül. |
| Svm | `19` | Svm dosyalarını okuyan modül. |
| MathML | `20` | W3C MathML dosyalarını okuyan modül. |
| Font | `21` | Yazı tipi dosyalarını okuyan modül. |
| Svg | `22` | SVG dosyalarını okuyan modül. |
| Markdown | `23` | Markdown dosyalarını okuyan/yazabilen modül. |
| Chm | `24` | CHM dosyalarını okuyan modül. |
| Epub | `25` | EPUB dosyalarını okuyan/yazabilen modül. |
| Xml | `26` | XML dosyalarını okuyan modül. |
| Xlsx | `27` | XLSX dosyalarını yazan modül. |

## Örnekler

Uyarı kaynağıyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
