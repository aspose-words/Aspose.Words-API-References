---
title: "FontSubstitutionSettings"
linktitle: "FontSubstitutionSettings"
second_title: "Aspose.Words para Java"
description: "Especifica la configuración del mecanismo de sustitución de fuentes en Java."
type: docs
weight: 337
url: /es/java/com.aspose.words/fontsubstitutionsettings/
---

**Inheritance:**
java.lang.Object
```
public class FontSubstitutionSettings
```

Especifica la configuración del mecanismo de sustitución de fuentes.

Para obtener más información, visite el artículo de documentación [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

El proceso de sustitución de fuentes consiste en varias reglas que se verifican una por una en un orden específico. Si la primera regla no puede resolver la fuente, se verifica la segunda regla y así sucesivamente.

El orden de las reglas es el siguiente: 1. Regla de sustitución de nombre de fuente (activada por defecto) 2. Regla de sustitución de configuración de fuente (desactivada por defecto) 3. Regla de sustitución de tabla (activada por defecto) 4. Regla de sustitución de información de fuente (activada por defecto) 5. Regla de fuente predeterminada (activada por defecto)

Ten en cuenta que la regla de sustitución de información de fuente siempre resolverá la fuente si [FontInfo](../../com.aspose.words/fontinfo/) está disponible y sobrescribirá la regla de fuente predeterminada. Si deseas usar la regla de fuente predeterminada, deberías desactivar la regla de sustitución de información de fuente.

Ten en cuenta que la regla de sustitución de configuración de fuente resolverá la fuente en la mayoría de los casos y, por lo tanto, sobrescribe todas las demás reglas.

 **Examples:** 

Muestra cómo acceder a la fuente del sistema de fuentes de un documento y establecer sustitutos de fuentes.

```

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());

 // By default, a blank document always contains a system font source.
 Assert.assertEquals(1, doc.getFontSettings().getFontsSources().length);

 SystemFontSource systemFontSource = (SystemFontSource) doc.getFontSettings().getFontsSources()[0];
 Assert.assertEquals(FontSourceType.SYSTEM_FONTS, systemFontSource.getType());
 Assert.assertEquals(0, systemFontSource.getPriority());

 if (SystemUtils.IS_OS_WINDOWS) {
     final String FONTS_PATH = "C:\\WINDOWS\\Fonts";
     Assert.assertEquals(FONTS_PATH.toLowerCase(), SystemFontSource.getSystemFontFolders()[0].toLowerCase());
 }

 for (String systemFontFolder : SystemFontSource.getSystemFontFolders()) {
     System.out.println(systemFontFolder);
 }

 // Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
 doc.getFontSettings().getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);
 doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().addSubstitutes("Kreon-Regular", "Calibri");

 Assert.assertEquals(1, IterableUtils.size(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")));
 Assert.assertTrue(IterableUtils.toString(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")).contains("Calibri"));

 // Alternatively, we could add a folder font source in which the corresponding folder contains the font.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false);
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{systemFontSource, folderFontSource});
 Assert.assertEquals(2, doc.getFontSettings().getFontsSources().length);

 // Resetting the font sources still leaves us with the system font source as well as our substitutes.
 doc.getFontSettings().resetFontSources();

 Assert.assertEquals(1, doc.getFontSettings().getFontsSources().length);
 Assert.assertEquals(FontSourceType.SYSTEM_FONTS, doc.getFontSettings().getFontsSources()[0].getType());
 Assert.assertEquals(1, IterableUtils.size(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")));
 Assert.assertTrue(doc.getFontSettings().getSubstitutionSettings().getFontNameSubstitution().getEnabled());
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Métodos

| Método | Descripción |
| --- | --- |
| [getDefaultFontSubstitution()](#getDefaultFontSubstitution) | Configuraciones relacionadas con la regla de sustitución de fuente predeterminada. |
| [getFontConfigSubstitution()](#getFontConfigSubstitution) | Configuraciones relacionadas con la regla de sustitución de configuración de fuente. |
| [getFontInfoSubstitution()](#getFontInfoSubstitution) | Configuraciones relacionadas con la regla de sustitución de información de fuente. |
| [getFontNameSubstitution()](#getFontNameSubstitution) | Configuraciones relacionadas con la regla de sustitución de nombre de fuente. |
| [getTableSubstitution()](#getTableSubstitution) | Configuraciones relacionadas con la regla de sustitución de tabla. |
### getDefaultFontSubstitution() {#getDefaultFontSubstitution}
```
public DefaultFontSubstitutionRule getDefaultFontSubstitution()
```


Configuraciones relacionadas con la regla de sustitución de fuente predeterminada.

 **Examples:** 

Muestra cómo establecer la regla de sustitución de fuentes predeterminada.

```

 Document doc = new Document();
 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);

 // Get the default substitution rule within FontSettings.
 // This rule will substitute all missing fonts with "Times New Roman".
 DefaultFontSubstitutionRule defaultFontSubstitutionRule = fontSettings.getSubstitutionSettings().getDefaultFontSubstitution();
 Assert.assertTrue(defaultFontSubstitutionRule.getEnabled());
 Assert.assertEquals("Times New Roman", defaultFontSubstitutionRule.getDefaultFontName());

 // Set the default font substitute to "Courier New".
 defaultFontSubstitutionRule.setDefaultFontName("Courier New");

 // Using a document builder, add some text in a font that we do not have to see the substitution take place,
 // and then render the result in a PDF.
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Missing Font");
 builder.writeln("Line written in a missing font, which will be substituted with Courier New.");

 doc.save(getArtifactsDir() + "FontSettings.DefaultFontSubstitutionRule.pdf");
 
```

**Returns:**
[DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule/) - The corresponding [DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule/) value.
### getFontConfigSubstitution() {#getFontConfigSubstitution}
```
public FontConfigSubstitutionRule getFontConfigSubstitution()
```


Configuraciones relacionadas con la regla de sustitución de configuración de fuente.

 **Examples:** 

Muestra la sustitución de configuración de fuentes dependiente del sistema operativo.

```

 FontSettings fontSettings = new FontSettings();
 FontConfigSubstitutionRule fontConfigSubstitution = fontSettings.getSubstitutionSettings().getFontConfigSubstitution();

 // The FontConfigSubstitutionRule object works differently on Windows/non-Windows platforms.
 // On Windows, it is unavailable.
 if (SystemUtils.IS_OS_WINDOWS) {
     Assert.assertFalse(fontConfigSubstitution.getEnabled());
     Assert.assertFalse(fontConfigSubstitution.isFontConfigAvailable());
 }

 // On Linux/Mac, we will have access to it, and will be able to perform operations.
 if (SystemUtils.IS_OS_LINUX) {
     Assert.assertTrue(fontConfigSubstitution.getEnabled());
     Assert.assertTrue(fontConfigSubstitution.isFontConfigAvailable());

     fontConfigSubstitution.resetCache();
 }
 
```

**Returns:**
[FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule/) - The corresponding [FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule/) value.
### getFontInfoSubstitution() {#getFontInfoSubstitution}
```
public FontInfoSubstitutionRule getFontInfoSubstitution()
```


Configuraciones relacionadas con la regla de sustitución de información de fuente.

 **Examples:** 

Muestra cómo establecer la propiedad para encontrar la coincidencia más cercana de una fuente faltante entre las fuentes disponibles.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```

**Returns:**
[FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule/) - The corresponding [FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule/) value.
### getFontNameSubstitution() {#getFontNameSubstitution}
```
public FontNameSubstitutionRule getFontNameSubstitution()
```


Configuraciones relacionadas con la regla de sustitución de nombre de fuente.

 **Examples:** 

Muestra cómo acceder a la fuente del sistema de fuentes de un documento y establecer sustitutos de fuentes.

```

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());

 // By default, a blank document always contains a system font source.
 Assert.assertEquals(1, doc.getFontSettings().getFontsSources().length);

 SystemFontSource systemFontSource = (SystemFontSource) doc.getFontSettings().getFontsSources()[0];
 Assert.assertEquals(FontSourceType.SYSTEM_FONTS, systemFontSource.getType());
 Assert.assertEquals(0, systemFontSource.getPriority());

 if (SystemUtils.IS_OS_WINDOWS) {
     final String FONTS_PATH = "C:\\WINDOWS\\Fonts";
     Assert.assertEquals(FONTS_PATH.toLowerCase(), SystemFontSource.getSystemFontFolders()[0].toLowerCase());
 }

 for (String systemFontFolder : SystemFontSource.getSystemFontFolders()) {
     System.out.println(systemFontFolder);
 }

 // Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
 doc.getFontSettings().getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);
 doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().addSubstitutes("Kreon-Regular", "Calibri");

 Assert.assertEquals(1, IterableUtils.size(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")));
 Assert.assertTrue(IterableUtils.toString(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")).contains("Calibri"));

 // Alternatively, we could add a folder font source in which the corresponding folder contains the font.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false);
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{systemFontSource, folderFontSource});
 Assert.assertEquals(2, doc.getFontSettings().getFontsSources().length);

 // Resetting the font sources still leaves us with the system font source as well as our substitutes.
 doc.getFontSettings().resetFontSources();

 Assert.assertEquals(1, doc.getFontSettings().getFontsSources().length);
 Assert.assertEquals(FontSourceType.SYSTEM_FONTS, doc.getFontSettings().getFontsSources()[0].getType());
 Assert.assertEquals(1, IterableUtils.size(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")));
 Assert.assertTrue(doc.getFontSettings().getSubstitutionSettings().getFontNameSubstitution().getEnabled());
 
```

**Returns:**
[FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule/) - The corresponding [FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule/) value.
### getTableSubstitution() {#getTableSubstitution}
```
public TableSubstitutionRule getTableSubstitution()
```


Configuraciones relacionadas con la regla de sustitución de tabla.

 **Examples:** 

Muestra cómo trabajar con tablas de sustitución de fuentes personalizadas.

```

 Document doc = new Document();
 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);

 // Create a new table substitution rule and load the default Windows font substitution table.
 TableSubstitutionRule tableSubstitutionRule = fontSettings.getSubstitutionSettings().getTableSubstitution();

 // If we select fonts exclusively from our folder, we will need a custom substitution table.
 // We will no longer have access to the Microsoft Windows fonts,
 // such as "Arial" or "Times New Roman" since they do not exist in our new font folder.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false);
 fontSettings.setFontsSources(new FontSourceBase[]{folderFontSource});

 // Below are two ways of loading a substitution table from a file in the local file system.
 // 1 -  From a stream:
 try (FileInputStream fileStream = new FileInputStream(getMyDir() + "Font substitution rules.xml")) {
     tableSubstitutionRule.load(fileStream);
 }

 // 2 -  Directly from a file:
 tableSubstitutionRule.load(getMyDir() + "Font substitution rules.xml");

 // Since we no longer have access to "Arial", our font table will first try substitute it with "Nonexistent Font".
 // We do not have this font so that it will move onto the next substitute, "Kreon", found in the "MyFonts" folder.
 Assert.assertEquals(new String[]{"Missing Font", "Kreon"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Arial")).toArray());

 // We can expand this table programmatically. We will add an entry that substitutes "Times New Roman" with "Arvo"
 Assert.assertNull(tableSubstitutionRule.getSubstitutes("Times New Roman"));
 tableSubstitutionRule.addSubstitutes("Times New Roman", "Arvo");
 Assert.assertEquals(new String[]{"Arvo"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // We can add a secondary fallback substitute for an existing font entry with AddSubstitutes().
 // In case "Arvo" is unavailable, our table will look for "M+ 2m" as a second substitute option.
 tableSubstitutionRule.addSubstitutes("Times New Roman", "M+ 2m");
 Assert.assertEquals(new String[]{"M+ 2m", "Arvo"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // SetSubstitutes() can set a new list of substitute fonts for a font.
 tableSubstitutionRule.setSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
 Assert.assertEquals(new String[]{"Squarish Sans CT", "M+ 2m"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // Writing text in fonts that we do not have access to will invoke our substitution rules.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Arial");
 builder.writeln("Text written in Arial, to be substituted by Kreon.");

 builder.getFont().setName("Times New Roman");
 builder.writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

 doc.save(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Custom.pdf");
 
```

**Returns:**
[TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule/) - The corresponding [TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule/) value.
