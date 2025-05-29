---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: .NET için Aspose.Words
description: ExpandTableStylesToDirectFormatting yöntemiyle tablo stillerini doğrudan biçimlendirmeye dönüştürün ve belgenizin görünümünü zahmetsizce geliştirin.
type: docs
weight: 630
url: /tr/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Tablo stillerinde belirtilen biçimlendirmeyi, belgedeki tablolarda doğrudan biçimlendirmeye dönüştürür.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## Notlar

Bu yöntem, Aspose.Words'ün bu sürümünün yalnızca sınırlı destek sağladığı için mevcuttur. tablo stilleri (aşağıya bakın). Bu yöntem, tablo stilleriyle biçimlendirilmiş tablolar içeren bir DOCX veya WordprocessingML belgesi yüklediğinizde ve tablolarının, hücrelerinin, paragraflarının veya metninin biçimlendirmesini sorgulamanız gerektiğinde yararlı olabilir.

Aspose.Words'ün bu sürümü aşağıdaki tablo stilleri için sınırlı destek sağlar:

* DOCX veya WordprocessingML belgelerinde tanımlanan tablo stilleri, belge DOCX veya WordprocessingML olarak kaydedildiğinde tablo styles olarak korunur.
* DOCX veya WordprocessingML belgelerinde tanımlanan tablo stilleri, belgeyi herhangi başka bir biçime kaydederken, oluştururken veya yazdırırken otomatik olarak tablolarda doğrudan biçimlendirmeye dönüştürülür .
* DOC belgelerinde tanımlanan tablo stilleri, belgeyi yalnızca DOC olarak kaydettiğinizde tablo stilleri olarak korunur.

## Örnekler

Bir tablonun stilinin özelliklerinin doğrudan tablonun elemanlarına nasıl uygulanacağını gösterir.

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

// Bu yöntem yukarıda belirlediğimiz gibi tablo stili özellikleriyle ilgilidir.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
