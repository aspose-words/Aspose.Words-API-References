---
title: ConvertUtil.millimeter_to_point method
linktitle: millimeter_to_point method
articleTitle: millimeter_to_point method
second_title: Aspose.Words for Python
description: "ConvertUtil.millimeter_to_point method. Converts millimeters to points."
type: docs
weight: 20
url: /tr/python-net/aspose.words/convertutil/millimeter_to_point/
---

## millimeter_to_point(millimeters) {#float}

Converts millimeters to points.


```python
def millimeter_to_point(self, millimeters: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| millimeters | float | The value to convert. |

### Remarks

1 inch equals 25.4 millimeters. 1 inch equals 72 points.


### Examples

Shows how to specify page properties in millimeters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir bölümün "Page Setup" (Sayfa Ayarı), sayfa kenar boşluklarının boyutunu puan cinsinden tanımlar.
# Ayrıca "ConvertUtil" sınıfını daha tanıdık bir ölçü birimi kullanmak için kullanabiliriz,
# örneğin sınırları tanımlarken milimetre gibi.
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.millimeter_to_point(30)
page_setup.bottom_margin = aw.ConvertUtil.millimeter_to_point(50)
page_setup.left_margin = aw.ConvertUtil.millimeter_to_point(80)
page_setup.right_margin = aw.ConvertUtil.millimeter_to_point(40)
# Bir santimetre yaklaşık 28,3 puandır.
self.assertAlmostEqual(28.34, aw.ConvertUtil.millimeter_to_point(10), delta=0.01)
# Yeni kenar boşluklarını göstermek için içerik ekleyin.
builder.writeln(f'This Text is {page_setup.left_margin} points from the left, ' + f'{page_setup.right_margin} points from the right, ' + f'{page_setup.top_margin} points from the top, ' + f'and {page_setup.bottom_margin} points from the bottom of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndMillimeters.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConvertUtil](../)

