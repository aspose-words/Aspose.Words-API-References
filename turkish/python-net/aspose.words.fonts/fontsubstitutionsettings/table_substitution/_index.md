---
title: FontSubstitutionSettings.table_substitution property
linktitle: table_substitution property
articleTitle: table_substitution property
second_title: Aspose.Words for Python
description: "FontSubstitutionSettings.table_substitution property. Settings related to table substitution rule."
type: docs
weight: 50
url: /tr/python-net/aspose.words.fonts/fontsubstitutionsettings/table_substitution/
---

## FontSubstitutionSettings.table_substitution property

Settings related to table substitution rule.


```python
@property
def table_substitution(self) -> aspose.words.fonts.TableSubstitutionRule:
    ...

```

### Examples

Shows how to work with custom font substitution tables.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# Yeni bir tablo ikame kuralı oluşturun ve varsayılan Windows yazı tipi ikame tablosunu yükleyin.
table_substitution_rule = font_settings.substitution_settings.table_substitution
# Yazı tiplerini yalnızca klasörümüzden seçersek, özel bir ikame tablosuna ihtiyacımız olacak.
# Microsoft Windows yazı tiplerine artık erişemeyeceğiz,
# "Arial" veya "Times New Roman" gibi, çünkü bunlar yeni yazı tipi klasörümüzde yok.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
font_settings.set_fonts_sources(sources=[folder_font_source])
# Aşağıda yerel dosya sistemindeki bir dosyadan ikame tablosu yüklemenin iki yolu verilmiştir.
# 1 -  Bir akıştan:
with system_helper.io.FileStream(MY_DIR + 'Font substitution rules.xml', system_helper.io.FileMode.OPEN) as file_stream:
    table_substitution_rule.load(stream=file_stream)
# 2 -  Doğrudan bir dosyadan:
table_substitution_rule.load(file_name=MY_DIR + 'Font substitution rules.xml')
# "Arial"a artık erişemediğimiz için, yazı tipi tablomuz önce onu "Nonexistent Font" ile ikame etmeye çalışacak.
# Bu yazı tipine sahip olmadığımız için, "MyFonts" klasöründe bulunan bir sonraki ikame olan "Kreon"a geçecek.
self.assertEqual(['Missing Font', 'Kreon'], table_substitution_rule.get_substitutes('Arial'))
# Bu tabloyu programlı olarak genişletebiliriz. "Times New Roman"ı "Arvo" ile ikame eden bir giriş ekleyeceğiz.
self.assertIsNone(table_substitution_rule.get_substitutes('Times New Roman'))
table_substitution_rule.add_substitutes('Times New Roman', ['Arvo'])
self.assertEqual(['Arvo'], table_substitution_rule.get_substitutes('Times New Roman'))
# Mevcut bir yazı tipi girdisi için ikincil bir yedek ikameyi AddSubstitutes() ile ekleyebiliriz.
# "Arvo" mevcut değilse, tablomuz ikinci ikame seçeneği olarak "M+ 2m"'yi arayacak.
table_substitution_rule.add_substitutes('Times New Roman', ['M+ 2m'])
self.assertEqual(['Arvo', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# SetSubstitutes(), bir yazı tipi için yeni bir ikame yazı tipleri listesi ayarlayabilir.
table_substitution_rule.set_substitutes('Times New Roman', ['Squarish Sans CT', 'M+ 2m'])
self.assertEqual(['Squarish Sans CT', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# Erişemediğimiz yazı tiplerinde metin yazmak, ikame kurallarımızı tetikleyecek.
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Text written in Arial, to be substituted by Kreon.')
builder.font.name = 'Times New Roman'
builder.writeln('Text written in Times New Roman, to be substituted by Squarish Sans CT.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitutionRule.Custom.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSubstitutionSettings](../)

