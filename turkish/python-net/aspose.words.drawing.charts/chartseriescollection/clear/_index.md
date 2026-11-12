---
title: ChartSeriesCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.clear method. Removes all [ChartSeries](../../chartseries/) from this collection."
type: docs
weight: 80
url: /tr/python-net/aspose.words.drawing.charts/chartseriescollection/clear/
---

## clear() {#default}

Removes all [ChartSeries](../../chartseries/) from this collection.



```python
def clear(self):
    ...
```

### Examples

Shows how to add and remove series data in a chart.

```python
# Varsayılan olarak üç demo veri serisi içerecek bir sütun grafik ekleyin.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=ChartType.COLUMN, width=400, height=300)
chart = chart_shape.chart
chart_data = chart.series
assert chart_data.count == 3
# Grafikteki her serinin adını yazdırın.
for series in chart.series:
    print(series.name)
# Bunlar, grafikteki kategorilerin adlarıdır.
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
# Mevcut kategoriler için yeni değerlerle bir seri ekleyebiliriz.
# Bu grafik artık dört sütunluk dört küme içerecek.
chart.series.add(series_name='Series 4', categories=categories, values=[4.4, 7, 3.5, 2.1])
assert chart_data.count == 4
assert chart_data[3].name == 'Series 4'
# Bir grafik serisi, indeksle de kaldırılabilir, şöyle.
# Bu, grafikle gelen üç demo serisinden birini kaldıracak.
chart_data.remove_at(2)
assert not any([s.name == 'Series 3' for s in chart_data])
assert chart_data.count == 3
assert chart_data[2].name == 'Series 4'
# Bu yöntemle grafiğin tüm verilerini bir kerede temizleyebiliriz.
# Yeni bir grafik oluştururken, tüm demo verileri silmenin yolu budur
# boş bir grafik üzerinde çalışmaya başlamadan önce.
chart_data.clear()
assert chart_data.count == 0
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

