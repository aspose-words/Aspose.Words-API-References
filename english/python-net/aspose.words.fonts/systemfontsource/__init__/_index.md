---
title: SystemFontSource constructor
linktitle: SystemFontSource constructor
articleTitle: SystemFontSource constructor
second_title: Aspose.Words for Python
description: "aspose.words.fonts.SystemFontSource constructor"
type: docs
weight: 10
url: /python-net/aspose.words.fonts/systemfontsource/__init__/
---

## SystemFontSource() {#default}

Ctor.


```python
def __init__(self):
    ...
```

## SystemFontSource(priority) {#int}

Ctor.


```python
def __init__(self, priority: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| priority | int | Font source priority. See the [FontSourceBase.priority](../../fontsourcebase/priority/) property description for more information. |

## Examples

Shows how to access a document's system font source and set font substitutes.

```python
import platform
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR

class TestFontSubstitution(ApiExampleBase):

    def test_font_substitution(self):
        doc = aw.Document()
        doc.font_settings = aw.fonts.FontSettings()
        # By default, a blank document always contains a system font source.
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
        # Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
        doc.font_settings.substitution_settings.font_info_substitution.enabled = True
        doc.font_settings.substitution_settings.table_substitution.add_substitutes('Kreon-Regular', ['Calibri'])
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertIn('Calibri', doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular'))
        # Alternatively, we could add a folder font source in which the corresponding folder contains the font.
        folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
        doc.font_settings.set_fonts_sources(sources=[system_font_source, folder_font_source])
        self.assertEqual(2, len(doc.font_settings.get_fonts_sources()))
        # Resetting the font sources still leaves us with the system font source as well as our substitutes.
        doc.font_settings.reset_font_sources()
        self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))
        self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, doc.font_settings.get_fonts_sources()[0].type)
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertTrue(doc.font_settings.substitution_settings.font_name_substitution.enabled)
```

## See Also

* module [aspose.words.fonts](../../)
* class [SystemFontSource](../)

