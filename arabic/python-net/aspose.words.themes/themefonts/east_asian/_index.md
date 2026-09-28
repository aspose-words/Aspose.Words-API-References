---
title: ThemeFonts.east_asian property
linktitle: east_asian property
articleTitle: east_asian property
second_title: Aspose.Words for Python
description: "ThemeFonts.east_asian property. Specifies font name for EastAsian characters."
type: docs
weight: 20
url: /ar/python-net/aspose.words.themes/themefonts/east_asian/
---

## ThemeFonts.east_asian property

Specifies font name for EastAsian characters.


```python
@property
def east_asian(self) -> str:
    ...

@east_asian.setter
def east_asian(self, value: str):
    ...

```

### Examples

Shows how to set custom colors and fonts for themes.

```python
doc = aw.Document(file_name=MY_DIR + 'Theme colors.docx')
# كائن "Theme" يمنحنا الوصول إلى سمة المستند، وهو مصدر الخطوط والألوان الافتراضية.
theme = doc.theme
# بعض الأنماط، مثل "Heading 1" و "Subtitle"، ستورث هذه الخطوط.
theme.major_fonts.latin = 'Courier New'
theme.minor_fonts.latin = 'Agency FB'
# قد تحتوي لغات أخرى أيضًا على خطوطها المخصصة في هذه السمة.
self.assertEqual('', theme.major_fonts.complex_script)
self.assertEqual('', theme.major_fonts.east_asian)
self.assertEqual('', theme.minor_fonts.complex_script)
self.assertEqual('', theme.minor_fonts.east_asian)
# خاصية "Colors" تحتوي على لوحة الألوان من Microsoft Word،
# التي تظهر عند تغيير التظليل أو لون الخط.
# طبق ألوانًا مخصصة على لوحة الألوان حتى نتمكن من الوصول إليها بسهولة في Microsoft Word
# عندما نقوم، على سبيل المثال، بتغيير لون الخط عبر "Home" -> "Font" -> "Font Color"،
# أو إدراج شكل، ثم تعيين لون له عبر "Shape Format" -> "Shape Styles".
colors = theme.colors
colors.dark1 = aspose.pydrawing.Color.midnight_blue
colors.light1 = aspose.pydrawing.Color.pale_green
colors.dark2 = aspose.pydrawing.Color.indigo
colors.light2 = aspose.pydrawing.Color.khaki
colors.accent1 = aspose.pydrawing.Color.orange_red
colors.accent2 = aspose.pydrawing.Color.light_salmon
colors.accent3 = aspose.pydrawing.Color.yellow
colors.accent4 = aspose.pydrawing.Color.gold
colors.accent5 = aspose.pydrawing.Color.blue_violet
colors.accent6 = aspose.pydrawing.Color.dark_violet
# طبق ألوانًا مخصصة على الروابط في حالتي النقر وعدم النقر.
colors.hyperlink = aspose.pydrawing.Color.black
colors.followed_hyperlink = aspose.pydrawing.Color.gray
doc.save(file_name=ARTIFACTS_DIR + 'Themes.CustomColorsAndFonts.docx')
```

### See Also

* module [aspose.words.themes](../../)
* class [ThemeFonts](../)

