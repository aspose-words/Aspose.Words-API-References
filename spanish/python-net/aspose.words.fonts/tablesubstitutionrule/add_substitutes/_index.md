---
title: TableSubstitutionRule.add_substitutes method
linktitle: add_substitutes method
articleTitle: add_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.add_substitutes method. Adds substitute font names for given original font name."
type: docs
weight: 10
url: /es/python-net/aspose.words.fonts/tablesubstitutionrule/add_substitutes/
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
        # De forma predeterminada, un documento en blanco siempre contiene una fuente tipográfica del sistema.
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
        # Establezca una fuente que exista en el directorio de fuentes de Windows como sustituta de una que no exista.
        doc.font_settings.substitution_settings.font_info_substitution.enabled = True
        doc.font_settings.substitution_settings.table_substitution.add_substitutes('Kreon-Regular', ['Calibri'])
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertIn('Calibri', doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular'))
        # Alternativamente, podríamos agregar una fuente tipográfica de carpeta en la que la carpeta correspondiente contenga la fuente.
        folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
        doc.font_settings.set_fonts_sources(sources=[system_font_source, folder_font_source])
        self.assertEqual(2, len(doc.font_settings.get_fonts_sources()))
        # Restablecer las fuentes tipográficas aún nos deja con la fuente tipográfica del sistema, así como con nuestras sustituciones.
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
# Crea una nueva regla de sustitución de tabla y carga la tabla de sustitución de fuentes predeterminada de Windows.
table_substitution_rule = font_settings.substitution_settings.table_substitution
# Si seleccionamos fuentes exclusivamente de nuestra carpeta, necesitaremos una tabla de sustitución personalizada.
# Ya no tendremos acceso a las fuentes de Microsoft Windows,
# como "Arial" o "Times New Roman" ya que no existen en nuestra nueva carpeta de fuentes.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
font_settings.set_fonts_sources(sources=[folder_font_source])
# A continuación se presentan dos formas de cargar una tabla de sustitución desde un archivo en el sistema de archivos local.
# 1 -  Desde un flujo:
with system_helper.io.FileStream(MY_DIR + 'Font substitution rules.xml', system_helper.io.FileMode.OPEN) as file_stream:
    table_substitution_rule.load(stream=file_stream)
# 2 -  Directamente desde un archivo:
table_substitution_rule.load(file_name=MY_DIR + 'Font substitution rules.xml')
# Dado que ya no tenemos acceso a "Arial", nuestra tabla de fuentes intentará primero sustituirla con "Nonexistent Font".
# No disponemos de esta fuente, por lo que pasará a la siguiente sustituta, "Kreon", encontrada en la carpeta "MyFonts".
self.assertEqual(['Missing Font', 'Kreon'], table_substitution_rule.get_substitutes('Arial'))
# Podemos expandir esta tabla programáticamente. Añadiremos una entrada que sustituya "Times New Roman" con "Arvo"
self.assertIsNone(table_substitution_rule.get_substitutes('Times New Roman'))
table_substitution_rule.add_substitutes('Times New Roman', ['Arvo'])
self.assertEqual(['Arvo'], table_substitution_rule.get_substitutes('Times New Roman'))
# Podemos agregar un sustituto de reserva secundario para una entrada de fuente existente con AddSubstitutes().
# En caso de que "Arvo" no esté disponible, nuestra tabla buscará "M+ 2m" como segunda opción de sustituto.
table_substitution_rule.add_substitutes('Times New Roman', ['M+ 2m'])
self.assertEqual(['Arvo', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# SetSubstitutes() puede establecer una nueva lista de fuentes sustitutas para una fuente.
table_substitution_rule.set_substitutes('Times New Roman', ['Squarish Sans CT', 'M+ 2m'])
self.assertEqual(['Squarish Sans CT', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# Escribir texto con fuentes a las que no tenemos acceso activará nuestras reglas de sustitución.
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

