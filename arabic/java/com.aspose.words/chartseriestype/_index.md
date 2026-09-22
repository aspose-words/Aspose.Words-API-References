---
title: "ChartSeriesType"
linktitle: "ChartSeriesType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع سلسلة مخطط في Java."
type: docs
weight: 89
url: /ar/java/com.aspose.words/chartseriestype/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesType
```

يحدد نوع سلسلة المخطط.

 **Examples:** 

يعرض كيفية إزالة سلسلة مخطط محددة.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 // Remove all series of the Column type.
 for (int i = chart.getSeries().getCount() - 1; i >= 0; i--)
 {
     if (chart.getSeries().get(i).getSeriesType() == ChartSeriesType.COLUMN)
         chart.getSeries().removeAt(i);
 }

 chart.getSeries().add(
         "Aspose Series",
         new String[] { "Category 1", "Category 2", "Category 3", "Category 4" },
         new double[] { 5.6, 7.1, 2.9, 8.9 });

 doc.save(getArtifactsDir() + "Charts.RemoveSpecificChartSeries.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AREA](#AREA) | يمثل سلسلة مخطط منطقة. |
| [AREA_3_D](#AREA-3-D) | يمثل سلسلة مخطط منطقة ثلاثية الأبعاد. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | يمثل سلسلة مخطط منطقة مكدسة 100% ثلاثية الأبعاد. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | يمثل سلسلة مخطط منطقة مكدسة ثلاثية الأبعاد. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | يمثل سلسلة مخطط منطقة مكدسة 100%. |
| [AREA_STACKED](#AREA-STACKED) | يمثل سلسلة مخطط منطقة مكدسة. |
| [BAR](#BAR) | يمثل سلسلة مخطط شريط. |
| [BAR_3_D](#BAR-3-D) | يمثل سلسلة مخطط شريط ثلاثية الأبعاد. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | يمثل سلسلة مخطط شريط مكدس 100% ثلاثية الأبعاد. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | يمثل سلسلة مخطط شريط مكدس ثلاثية الأبعاد. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | يمثل سلسلة مخطط شريط مكدس 100%. |
| [BAR_STACKED](#BAR-STACKED) | يمثل سلسلة مخطط شريط مكدس. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | يمثل سلسلة مخطط صندوق وشارب. |
| [BUBBLE](#BUBBLE) | يمثل سلسلة مخطط فقاعة. |
| [BUBBLE_3_D](#BUBBLE-3-D) | يمثل سلسلة مخطط فقاعة ثلاثية الأبعاد. |
| [COLUMN](#COLUMN) | يمثل سلسلة مخطط عمود. |
| [COLUMN_3_D](#COLUMN-3-D) | يمثل سلسلة مخطط عمودي ثلاثي الأبعاد. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | يمثل سلسلة مخطط عمودي ثلاثي الأبعاد مجمع. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | يمثل سلسلة مخطط عمودي ثلاثي الأبعاد مكدس بنسبة 100٪. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | يمثل سلسلة مخطط عمودي ثلاثي الأبعاد مكدس. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | يمثل سلسلة مخطط عمودي مكدس بنسبة 100٪. |
| [COLUMN_STACKED](#COLUMN-STACKED) | يمثل سلسلة مخطط عمودي مكدس. |
| [DOUGHNUT](#DOUGHNUT) | يمثل سلسلة مخطط دونات. |
| [FUNNEL](#FUNNEL) | يمثل سلسلة مخطط قمع. |
| [HISTOGRAM](#HISTOGRAM) | يمثل سلسلة مخطط هيستوجرام. |
| [LINE](#LINE) | يمثل سلسلة مخطط خطي. |
| [LINE_3_D](#LINE-3-D) | يمثل سلسلة مخطط خطي ثلاثي الأبعاد. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | يمثل سلسلة مخطط خطي مكدس بنسبة 100٪. |
| [LINE_STACKED](#LINE-STACKED) | يمثل سلسلة مخطط خطي مكدس. |
| [PARETO](#PARETO) | يمثل سلسلة مخطط باريتو. |
| [PARETO_LINE](#PARETO-LINE) | يمثل سلسلة مخطط خطي باريتو. |
| [PIE](#PIE) | يمثل سلسلة مخطط دائري. |
| [PIE_3_D](#PIE-3-D) | يمثل سلسلة مخطط دائري ثلاثي الأبعاد. |
| [PIE_OF_BAR](#PIE-OF-BAR) | يمثل سلسلة مخطط دائري من شريط. |
| [PIE_OF_PIE](#PIE-OF-PIE) | يمثل سلسلة مخطط دائري من دائري. |
| [RADAR](#RADAR) | يمثل سلسلة مخطط رادار. |
| [REGION_MAP](#REGION-MAP) | يمثل سلسلة مخطط خريطة إقليمية. |
| [SCATTER](#SCATTER) | يمثل سلسلة مخطط مبعثر. |
| [STOCK](#STOCK) | يمثل سلسلة مخطط أسهم. |
| [SUNBURST](#SUNBURST) | يمثل سلسلة مخطط شمسية. |
| [SURFACE](#SURFACE) | يمثل سلسلة مخطط سطحي. |
| [SURFACE_3_D](#SURFACE-3-D) | يمثل سلسلة مخطط سطح ثلاثي الأبعاد. |
| [TREEMAP](#TREEMAP) | يمثل سلسلة مخطط شجرة. |
| [WATERFALL](#WATERFALL) | يمثل سلسلة مخطط شلال. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String chartSeriesTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartSeriesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartSeriesType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


يمثل سلسلة مخطط منطقة.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


يمثل سلسلة مخطط منطقة ثلاثية الأبعاد.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


يمثل سلسلة مخطط منطقة مكدسة 100% ثلاثية الأبعاد.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


يمثل سلسلة مخطط منطقة مكدسة ثلاثية الأبعاد.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


يمثل سلسلة مخطط منطقة مكدسة 100%.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


يمثل سلسلة مخطط منطقة مكدسة.

### BAR {#BAR}
```
public static int BAR
```


يمثل سلسلة مخطط شريط.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


يمثل سلسلة مخطط شريط ثلاثية الأبعاد.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


يمثل سلسلة مخطط شريط مكدس 100% ثلاثية الأبعاد.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


يمثل سلسلة مخطط شريط مكدس ثلاثية الأبعاد.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


يمثل سلسلة مخطط شريط مكدس 100%.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


يمثل سلسلة مخطط شريط مكدس.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


يمثل سلسلة مخطط صندوق وشارب.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


يمثل سلسلة مخطط فقاعة.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


يمثل سلسلة مخطط فقاعة ثلاثية الأبعاد.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


يمثل سلسلة مخطط عمود.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


يمثل سلسلة مخطط عمودي ثلاثي الأبعاد.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


يمثل سلسلة مخطط عمودي ثلاثي الأبعاد مجمع.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


يمثل سلسلة مخطط عمودي ثلاثي الأبعاد مكدس بنسبة 100٪.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


يمثل سلسلة مخطط عمودي ثلاثي الأبعاد مكدس.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


يمثل سلسلة مخطط عمودي مكدس بنسبة 100٪.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


يمثل سلسلة مخطط عمودي مكدس.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


يمثل سلسلة مخطط دونات.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


يمثل سلسلة مخطط قمع.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


يمثل سلسلة مخطط هيستوجرام.

### LINE {#LINE}
```
public static int LINE
```


يمثل سلسلة مخطط خطي.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


يمثل سلسلة مخطط خطي ثلاثي الأبعاد.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


يمثل سلسلة مخطط خطي مكدس بنسبة 100٪.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


يمثل سلسلة مخطط خطي مكدس.

### PARETO {#PARETO}
```
public static int PARETO
```


يمثل سلسلة مخطط باريتو.

### PARETO_LINE {#PARETO-LINE}
```
public static int PARETO_LINE
```


يمثل سلسلة مخطط خطي باريتو.

### PIE {#PIE}
```
public static int PIE
```


يمثل سلسلة مخطط دائري.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


يمثل سلسلة مخطط دائري ثلاثي الأبعاد.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


يمثل سلسلة مخطط دائري من شريط.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


يمثل سلسلة مخطط دائري من دائري.

### RADAR {#RADAR}
```
public static int RADAR
```


يمثل سلسلة مخطط رادار.

### REGION_MAP {#REGION-MAP}
```
public static int REGION_MAP
```


يمثل سلسلة مخطط خريطة إقليمية.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


يمثل سلسلة مخطط مبعثر.

### STOCK {#STOCK}
```
public static int STOCK
```


يمثل سلسلة مخطط أسهم.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


يمثل سلسلة مخطط شمسية.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


يمثل سلسلة مخطط سطحي.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


يمثل سلسلة مخطط سطح ثلاثي الأبعاد.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


يمثل سلسلة مخطط شجرة.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


يمثل سلسلة مخطط شلال.

### length {#length}
```
public static int length
```


### fromName(String chartSeriesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartSeriesTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartSeriesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartSeriesType) {#getName-int}
```
public static String getName(int chartSeriesType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartSeriesType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartSeriesType) {#toString-int}
```
public static String toString(int chartSeriesType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartSeriesType | int |  |

**Returns:**
java.lang.String
