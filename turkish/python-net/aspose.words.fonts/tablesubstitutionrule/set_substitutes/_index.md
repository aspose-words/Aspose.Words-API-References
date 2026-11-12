---
title: TableSubstitutionRule.set_substitutes method
linktitle: set_substitutes method
articleTitle: set_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.set_substitutes method. Override substitute font names for given original font name."
type: docs
weight: 80
url: /tr/python-net/aspose.words.fonts/tablesubstitutionrule/set_substitutes/
---

## set_substitutes(original_font_name, substitute_font_names) {#str_strlist}

Override substitute font names for given original font name.


```python
def set_substitutes(self, original_font_name: str, substitute_font_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| original_font_name | str | Original font name. |
| substitute_font_names | List[str] | List of alternative font names. |

### Examples

Shows how set font substitution rules.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# Varsayılan yazı tipi kaynakları, belgenin kullandığı ilk yazı tipini içerir.
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
# İkinci yazı tipi, "Amethysta", mevcut değil.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in font_sources[0].get_available_fonts()]))
# Yazı tipi ikame tablosunu yapılandırabiliriz ve bu tablo belirler
# hangi yazı tiplerinin Aspose.Words tarafından mevcut olmayan yazı tipleri için ikame olarak kullanılacağını.
# "Amethysta" için iki ikame yazı tipini ayarlayın: "Arvo" ve "Courier New".
# İlk ikame mevcut değilse, Aspose.Words ikinci ikameyi kullanmayı dener ve bu şekilde devam eder.
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# "Amethysta" mevcut değil ve ikame kuralı, ikame olarak kullanılacak ilk yazı tipinin "Arvo" olduğunu belirtir.
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# "Arvo" da mevcut değil, ancak "Courier New" mevcut.
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# Çıktı belgesi, "Amethysta" yazı tipini kullanan metni "Courier New" ile biçimlendirilmiş olarak gösterecek.
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitution.pdf')
```

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
* class [TableSubstitutionRule](../)

