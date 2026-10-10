---
title: "ChartLegendEntry"
linktitle: "ChartLegendEntry"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafik lejand girişi temsil eder."
type: docs
weight: 80
url: /tr/java/com.aspose.words/chartlegendentry/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartLegendEntry implements Cloneable
```

Grafik lejand girdisini temsil eder.

Daha fazla bilgi için, [ Working with Charts ][Working with Charts] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bir lejand girişi belirli bir grafik serisi veya eğriye karşılık gelir.

Girişin metni, serinin veya eğrinin adıdır. Metin değiştirilemez.

 **Examples:** 

Lejant yazı tipiyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 ChartLegend chartLegend = chart.getLegend();
 // Set default font size all legend entries.
 chartLegend.getFont().setSize(14.0);
 // Change font for specific legend entry.
 chartLegend.getLegendEntries().get(1).getFont().setItalic(true);
 chartLegend.getLegendEntries().get(1).getFont().setSize(12.0);
 // Get legend entry for chart series.
 ChartLegendEntry legendEntry = chart.getSeries().get(0).getLegendEntry();

 doc.save(getArtifactsDir() + "Charts.LegendFont.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | Bu lejand girişinin yazı tipi biçimlendirmesine erişim sağlar. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [isHidden()](#isHidden) | Bu girişin grafik lejandında gizli olup olmadığını gösteren bir değeri alır. |
| [isHidden(boolean value)](#isHidden-boolean) | Bu girişin grafik lejandında gizli olup olmadığını gösteren bir değeri ayarlar. |
### fetchSpecialDefaultRunPropertyValue(int key) {#fetchSpecialDefaultRunPropertyValue-int}
```
public Object fetchSpecialDefaultRunPropertyValue(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### generateItemText() {#generateItemText}
```
public String generateItemText()
```




**Returns:**
java.lang.String
### getFont() {#getFont}
```
public Font getFont()
```


Bu lejand girişinin yazı tipi biçimlendirmesine erişim sağlar.

 **Examples:** 

Lejant yazı tipiyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 ChartLegend chartLegend = chart.getLegend();
 // Set default font size all legend entries.
 chartLegend.getFont().setSize(14.0);
 // Change font for specific legend entry.
 chartLegend.getLegendEntries().get(1).getFont().setItalic(true);
 chartLegend.getLegendEntries().get(1).getFont().setSize(12.0);
 // Get legend entry for chart series.
 ChartLegendEntry legendEntry = chart.getSeries().get(0).getLegendEntry();

 doc.save(getArtifactsDir() + "Charts.LegendFont.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getRelativePropertyValue(int key, Object value) {#getRelativePropertyValue-int-java.lang.Object}
```
public Object getRelativePropertyValue(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

**Returns:**
java.lang.Object
### isHidden() {#isHidden}
```
public boolean isHidden()
```


Bu girişin grafik lejandında gizli olup olmadığını gösteren bir değeri alır. Varsayılan değer **false**'dur.

 **Remarks:** 

Bir grafik lejand girişi gizlendiğinde, grafikte hâlâ görüntülenen ilgili grafik serisi veya eğriyi etkilemez.

 **Examples:** 

Grafik serileri için bir açıklama girişiyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "AW Category 1", "AW Category 2" };

 ChartSeries series1 = series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });
 series.add("Series 3", categories, new double[] { 5.0, 6.0 });
 series.add("Series 4", categories, new double[] { 0.0, 0.0 });

 ChartLegendEntryCollection legendEntries = chart.getLegend().getLegendEntries();
 legendEntries.get(3).isHidden(true);

 doc.save(getArtifactsDir() + "Charts.LegendEntries.docx");
 
```

**Returns:**
boolean - Bu girişin grafik lejandında gizli olup olmadığını gösteren bir değer.
### isHidden(boolean value) {#isHidden-boolean}
```
public void isHidden(boolean value)
```


Bu girişin grafik lejandında gizli olup olmadığını gösteren bir değeri ayarlar. Varsayılan değer **false**'dur.

 **Remarks:** 

Bir grafik lejand girişi gizlendiğinde, grafikte hâlâ görüntülenen ilgili grafik serisi veya eğriyi etkilemez.

 **Examples:** 

Grafik serileri için bir açıklama girişiyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "AW Category 1", "AW Category 2" };

 ChartSeries series1 = series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });
 series.add("Series 3", categories, new double[] { 5.0, 6.0 });
 series.add("Series 4", categories, new double[] { 0.0, 0.0 });

 ChartLegendEntryCollection legendEntries = chart.getLegend().getLegendEntries();
 legendEntries.get(3).isHidden(true);

 doc.save(getArtifactsDir() + "Charts.LegendEntries.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bu girişin grafik lejandında gizli olup olmadığını gösteren bir değer. |

