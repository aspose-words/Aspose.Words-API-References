---
title: OoxmlSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words for .NET
description: OoxmlSaveOptions Compliance mülk. Çıktı belgesinin OOXML sürümünü belirtir. Varsayılan değerEcma376_2006  C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/ooxmlsaveoptions/compliance/
---
## OoxmlSaveOptions.Compliance property

Çıktı belgesinin OOXML sürümünü belirtir. Varsayılan değer:Ecma376_2006 .

```csharp
public OoxmlCompliance Compliance { get; set; }
```

## Örnekler

DML şekillerinin bir belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü verilmiştir.
// 1 - Kayan:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Satır içi:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi "ilkel olmayan" şekiller oluşturmanız gerekiyorsa,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded veya DiagonalCornersRounded,
// daha sonra belgeyi, şeklin DML olarak kaydedilmesine olanak tanıyan "Katı" veya "Geçişli" uyumlulukla kaydedin.
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
// belgenin OOXML uyumluluk düzeyi "OoxmlComplianceCore.Ecma376"dan daha yeni bir standarttır.
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

Kaydedilen bir belge için uyulması gereken OOXML uyumluluk spesifikasyonunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Uyumluluk seçeneklerini Microsoft Word 2003'e uyacak şekilde yapılandırırsak,
// bir görüntünün eklenmesi, VML kullanılarak şeklinin tanımlanmasını sağlayacaktır.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// "ISO/IEC 29500:2008" OOXML standardı VML şekillerini desteklemez.
// SaveOptions nesnesinin "Compliance" özelliğini "OoxmlCompliance.Iso29500_2008_Strict" olarak ayarlarsak,
 // bu nesneyi geçerken kaydettiğimiz herhangi bir belgenin bu standarda uyması gerekecek.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Kaydedilen belgemiz, "ISO/IEC 29500:2008" OOXML standardına uymak için DML kullanarak şekli tanımlar.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Ayrıca bakınız

* enum [OoxmlCompliance](../../ooxmlcompliance/)
* class [OoxmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
