---
title: SystemFontSource class
linktitle: SystemFontSource class
articleTitle: SystemFontSource class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.SystemFontSource class. Represents all TrueType fonts installed to the system"
type: docs
weight: 240
url: /python-net/aspose.words.fonts/systemfontsource/
---

## SystemFontSource class

Represents all TrueType fonts installed to the system.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




**Inheritance:** [SystemFontSource](./) → [FontSourceBase](../fontsourcebase/)

### Constructors
| Name | Description |
| --- | --- |
| [SystemFontSource()](./__init__/#default) | Ctor. |
| [SystemFontSource(priority)](./__init__/#int) | Ctor. |

### Properties

| Name | Description |
| --- | --- |
| [priority](../fontsourcebase/priority/) | Returns the font source priority.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
| [type](./type/) | Returns the type of the font source. |
| [warning_callback](../fontsourcebase/warning_callback/) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_available_fonts()](../fontsourcebase/get_available_fonts/#default) | Returns list of fonts available via this source.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
|[ get_system_font_folders()](./get_system_font_folders/#default) | Returns system font folders or empty array if folders are not accessible. |

### Examples

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

### See Also

* module [aspose.words.fonts](../)
* class [FontSourceBase](../fontsourcebase/)

