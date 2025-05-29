---
title: OoxmlCompliance Enum
linktitle: OoxmlCompliance
articleTitle: OoxmlCompliance
second_title: .NET için Aspose.Words
description: En iyi DOCX formatını kaydetmek için tercih ettiğiniz OOXML spesifikasyonunu seçmek üzere Aspose.Words.Saving.OoxmlCompliance enum'unu keşfedin. Belge kalitesini bugün artırın!
type: docs
weight: 6120
url: /tr/net/aspose.words.saving/ooxmlcompliance/
---
## OoxmlCompliance enumeration

DOCX formatında kaydederken hangi OOXML spesifikasyonunun kullanılacağını belirtmeye izin verir.

```csharp
public enum OoxmlCompliance
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Ecma376_2006 | `0` | ECMA-376 1. Baskı, 2006. |
| Iso29500_2008_Transitional | `1` | ISO/IEC 29500:2008 Geçiş uyumluluk düzeyi. |
| Iso29500_2008_Strict | `2` | ISO/IEC 29500:2008 Sıkı uyumluluk seviyesi. |

## Örnekler

DML şekillerinin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
// 1 - Yüzen:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Satır içi:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi "ilkel olmayan" şekiller oluşturmanız gerekiyorsa,
// ÜstKöşelerBirYuvarlakBirKesilmiş, TekKöşeYuvarlak, ÜstKöşelerYuvarlak veya ÇaprazKöşelerYuvarlak,
// daha sonra belgeyi "Sıkı" veya "Geçiş" uyumluluğuyla kaydedin, bu da şeklin DML olarak kaydedilmesine olanak tanır.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

Her bölümde numaralandırmayı yeniden başlatmak için bir listenin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// "IsRestartAtEachSection" özelliği yalnızca şu durumlarda geçerli olacaktır:
// belgenin OOXML uyumluluk düzeyi "OoxmlComplianceCore.Ecma376" standardından daha yeni bir standarda uygundur.
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

Kaydedilen bir belgenin uyması gereken OOXML uyumluluk spesifikasyonunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Uyumluluk seçeneklerini Microsoft Word 2003 ile uyumlu olacak şekilde yapılandırırsak,
// Bir resim eklemek, VML kullanılarak şeklinin tanımlanmasını sağlayacaktır.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// "ISO/IEC 29500:2008" OOXML standardı VML şekillerini desteklemez.
// SaveOptions nesnesinin "Compliance" özelliğini "OoxmlCompliance.Iso29500_2008_Strict" olarak ayarlarsak,
 // Bu nesneyi geçirirken kaydettiğimiz her belgenin o standarda uyması gerekecektir.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Kaydedilen belgemiz, "ISO/IEC 29500:2008" OOXML standardına uymak için şekli DML kullanarak tanımlar.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
