---
title: Theme.colors property
linktitle: colors property
articleTitle: colors property
second_title: Aspose.Words for Python
description: "Theme.colors property. Allows to specify the set of theme colors for the document."
type: docs
weight: 20
url: /tr/python-net/aspose.words.themes/theme/colors/
---

## Theme.colors property

Allows to specify the set of theme colors for the document.


```python
@property
def colors(self) -> aspose.words.themes.ThemeColors:
    ...

```

### Examples

Shows how to set custom colors and fonts for themes.

```python
doc = aw.Document(file_name=MY_DIR + 'Theme colors.docx')
# The "Theme" nesnesi, belge temasına erişim sağlar; bu, varsayılan yazı tipleri ve renklerin kaynağıdır.
theme = doc.theme
# Bazı stiller, örneğin "Heading 1" ve "Subtitle", bu yazı tiplerini miras alacaktır.
theme.major_fonts.latin = 'Courier New'
theme.minor_fonts.latin = 'Agency FB'
# Diğer diller de bu temada kendi özel yazı tiplerine sahip olabilir.
self.assertEqual('', theme.major_fonts.complex_script)
self.assertEqual('', theme.major_fonts.east_asian)
self.assertEqual('', theme.minor_fonts.complex_script)
self.assertEqual('', theme.minor_fonts.east_asian)
# "Colors" özelliği, Microsoft Word'den renk paletini içerir,
# ki bu, gölgelendirme veya yazı tipi rengini değiştirirken görünür.
# Renk paletine özel renkler uygulayın, böylece Microsoft Word'de onlara kolayca erişebiliriz
# örneğin, "Home" -> "Font" -> "Font Color" yoluyla yazı tipi rengini değiştirdiğimizde,
# veya bir şekil ekleyip, ardından "Shape Format" -> "Shape Styles" aracılığıyla ona bir renk atadığınızda.
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
# Köprülerin tıklanmış ve tıklanmamış durumlarında özel renkler uygulayın.
colors.hyperlink = aspose.pydrawing.Color.black
colors.followed_hyperlink = aspose.pydrawing.Color.gray
doc.save(file_name=ARTIFACTS_DIR + 'Themes.CustomColorsAndFonts.docx')
```

### See Also

* module [aspose.words.themes](../../)
* class [Theme](../)

