---
title: Style.built_in property
linktitle: built_in property
articleTitle: built_in property
second_title: Aspose.Words for Python
description: "Style.built_in property. True if this style is one of the built-in styles in MS Word."
type: docs
weight: 40
url: /ar/python-net/aspose.words/style/built_in/
---

## Style.built_in property

True if this style is one of the built-in styles in MS Word.


```python
@property
def built_in(self) -> bool:
    ...

```

### Examples

Shows how to differentiate custom styles from built-in styles.

```python
doc = aw.Document()
# عند إنشاء مستند باستخدام Microsoft Word، أو برمجياً باستخدام Aspose.Words،
# سيأتي المستند مع مجموعة من الأنماط لتطبيقها على النص لتعديل مظهره.
# يمكننا الوصول إلى هذه الأنماط المدمجة عبر مجموعة "Styles" الخاصة بالمستند.
# ستحمل جميع هذه الأنماط العلامة "BuiltIn" مضبوطة على "true".
style = doc.styles.get_by_name('Emphasis')
self.assertTrue(style.built_in)
# إنشاء نمط مخصص وإضافته إلى المجموعة.
# الأنماط المخصصة مثل هذا ستحمل العلامة "BuiltIn" مضبوطة على "false".
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.navy
style.font.name = 'Courier New'
self.assertFalse(style.built_in)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

