---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words for .NET
description: Document ExpandTableStylesToDirectFormatting yöntem. Tablo stillerinde belirtilen biçimlendirmeyi belgedeki tablolardaki doğrudan biçimlendirmeye dönüştürür C#'da.
type: docs
weight: 590
url: /tr/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Tablo stillerinde belirtilen biçimlendirmeyi, belgedeki tablolardaki doğrudan biçimlendirmeye dönüştürür.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## Notlar

Bu yöntem, Aspose.Words'ün bu sürümünün tablo stilleri için yalnızca sınırlı destek sağlaması nedeniyle mevcuttur (aşağıya bakın). Bu yöntem, tablo stilleriyle biçimlendirilmiş tablolar içeren bir DOCX veya WordprocessingML belgesi yüklediğinizde ve tabloların, hücrelerin, paragrafların veya metnin biçimlendirmesini sorgulamanız gerektiğinde yararlı olabilir.

Aspose.Words'ün bu sürümü aşağıdaki tablo stilleri için sınırlı destek sağlar:

* DOCX veya WordprocessingML belgelerinde tanımlanan tablo stilleri, belge DOCX veya WordprocessingML olarak kaydedilirken tablo stilleri olarak korunur.
* DOCX veya WordprocessingML belgelerinde tanımlanan tablo stilleri, belgeyi başka herhangi bir formatta kaydederken, oluşturma veya yazdırma sırasında otomatik olarak tablolardaki doğrudan formatlamaya dönüştürülür.
* DOC belgelerinde tanımlanan tablo stilleri, belgeyi yalnızca DOC olarak kaydederken tablo stilleri olarak korunur.

## Örnekler

Bir tablonun stilinin özelliklerinin doğrudan tablonun öğelerine nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// Bu yöntem yukarıda belirlediğimiz tablo stili özellikleriyle ilgilidir.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
