---
title: "ChartAxisCollection"
linktitle: "ChartAxisCollection"
second_title: "Aspose.Words for Java"
description: "表示 Java 中图表轴的集合。"
type: docs
weight: 68
url: /zh/java/com.aspose.words/chartaxiscollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartAxisCollection implements Iterable
```

表示图表轴的集合。

 **Examples:** 

展示如何使用轴集合。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Hide the major grid lines on the primary and secondary Y axes.
 for (ChartAxis axis : chart.getAxes())
 {
     if (axis.getType() == ChartAxisType.VALUE)
         axis.hasMajorGridlines(false);
 }

 doc.save(getArtifactsDir() + "Charts.AxisCollection.docx");
 
```
## 方法

| 方法 | 描述 |
| --- | --- |
| [get(int index)](#get-int) | 获取指定索引处的轴。 |
| [getCount()](#getCount) | 获取此集合中轴的数量。 |
| [iterator()](#iterator) | 返回一个枚举器对象。 |
### get(int index) {#get-int}
```
public ChartAxis get(int index)
```


获取指定索引处的轴。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 索引 | int |  |

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The axis at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


获取此集合中轴的数量。

**Returns:**
int - 此集合中轴的数量。
### iterator() {#iterator}
```
public Iterator iterator()
```


返回一个枚举器对象。

**Returns:**
java.util.Iterator
