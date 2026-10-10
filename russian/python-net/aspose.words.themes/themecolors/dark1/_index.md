---
title: ThemeColors.dark1 property
linktitle: dark1 property
articleTitle: dark1 property
second_title: Aspose.Words for Python
description: "ThemeColors.dark1 property. Specifies color Dark 1."
type: docs
weight: 70
url: /ru/python-net/aspose.words.themes/themecolors/dark1/
---

## ThemeColors.dark1 property

Specifies color Dark 1.


```python
@property
def dark1(self) -> aspose.pydrawing.Color:
    ...

@dark1.setter
def dark1(self, value: aspose.pydrawing.Color):
    ...

```

### Examples

Shows how to set custom colors and fonts for themes.

```python
doc = aw.Document(file_name=MY_DIR + 'Theme colors.docx')
# Объект "Theme" предоставляет нам доступ к теме документа, источнику шрифтов и цветов по умолчанию.
theme = doc.theme
# Некоторые стили, такие как "Heading 1" и "Subtitle", будут наследовать эти шрифты.
theme.major_fonts.latin = 'Courier New'
theme.minor_fonts.latin = 'Agency FB'
# Другие языки также могут иметь свои пользовательские шрифты в этой теме.
self.assertEqual('', theme.major_fonts.complex_script)
self.assertEqual('', theme.major_fonts.east_asian)
self.assertEqual('', theme.minor_fonts.complex_script)
self.assertEqual('', theme.minor_fonts.east_asian)
# Свойство "Colors" содержит палитру цветов из Microsoft Word,
# которая появляется при изменении заливки или цвета шрифта.
# Примените пользовательские цвета к палитре, чтобы иметь к ним простой доступ в Microsoft Word
# когда мы, например, меняем цвет шрифта через "Home" -> "Font" -> "Font Color",
# или вставляем форму и затем задаём её цвет через "Shape Format" -> "Shape Styles".
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
# Примените пользовательские цвета к гиперссылкам в их состояниях после клика и без клика.
colors.hyperlink = aspose.pydrawing.Color.black
colors.followed_hyperlink = aspose.pydrawing.Color.gray
doc.save(file_name=ARTIFACTS_DIR + 'Themes.CustomColorsAndFonts.docx')
```

### See Also

* module [aspose.words.themes](../../)
* class [ThemeColors](../)

