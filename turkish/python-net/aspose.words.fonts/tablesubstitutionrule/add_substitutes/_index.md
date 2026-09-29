---
title: TableSubstitutionRule.add_substitutes method
linktitle: add_substitutes method
articleTitle: add_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.add_substitutes method. Adds substitute font names for given original font name."
type: docs
weight: 10
url: /tr/python-net/aspose.words.fonts/tablesubstitutionrule/add_substitutes/
---

## add_substitutes(original_font_name, substitute_font_names) {#str_strlist}

Adds substitute font names for given original font name.


```python
def add_substitutes(self, original_font_name: str, substitute_font_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| original_font_name | str | Original font name. |
| substitute_font_names | List[str] | List of alternative font names. |

### Examples

Shows how to access a document's system font source and set font substitutes.

```python
import platform
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR

class TestFontSubstitution(ApiExampleBase):

    def test_font_substitution(self):
        doc = aw.Document()
        doc.font_settings = aw.fonts.FontSettings()
        # Varsayılan olarak, boş bir belge her zaman bir sistem font kaynağı içerir.
        self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))
        system_font_source = doc.font_settings.get_fonts_sources()[0].as_system_font_source()
        self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, system_font_source.type)
        self.assertEqual(0, system_font_source.priority)
        is_windows = platform.system() == 'Windows'
        if is_windows:
            fonts_path = 'C:\\WINDOWS\\Fonts'
            actual = None
            cond_expression = next(iter(aw.fonts.SystemFontSource.get_system_font_folders()), None)
            if cond_expression is not None:
                actual = cond_expression.lower()
            self.assertEqual(fonts_path.lower(), actual)
        for system_font_folder in aw.fonts.SystemFontSource.get_system_font_folders():
            print(system_font_folder)
        # Windows Fonts dizininde bulunan bir fontu, bulunmayan bir fontun yerine geçecek şekilde ayarlayın.
        doc.font_settings.substitution_settings.font_info_substitution.enabled = True
        doc.font_settings.substitution_settings.table_substitution.add_substitutes('Kreon-Regular', ['Calibri'])
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertIn('Calibri', doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular'))
        # Alternatif olarak, ilgili klasörün fontu içerdiği bir klasör font kaynağı ekleyebiliriz.
        folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
        doc.font_settings.set_fonts_sources(sources=[system_font_source, folder_font_source])
        self.assertEqual(2, len(doc.font_settings.get_fonts_sources()))
        # Font kaynaklarını sıfırlamak, hâlâ sistem font kaynağını ve bizim yedeklerimizi bırakır.
        doc.font_settings.reset_font_sources()
        self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))
        self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, doc.font_settings.get_fonts_sources()[0].type)
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertTrue(doc.font_settings.substitution_settings.font_name_substitution.enabled)
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

