---
title: "WarningInfo"
linktitle: "WarningInfo"
second_title: "Aspose.Words لـ Java"
description: "يحتوي على معلومات حول التحذير الذي أصدرته Aspose.Words أثناء تحميل أو حفظ المستند في Java."
type: docs
weight: 717
url: /ar/java/com.aspose.words/warninginfo/
---

**Inheritance:**
java.lang.Object
```
public class WarningInfo
```

يحتوي على معلومات حول تحذير أصدره Aspose.Words أثناء تحميل أو حفظ المستند.

لمزيد من المعلومات، زر مقالة الوثائق [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

أنت لا تنشئ مثيلات من هذه الفئة. يتم إنشاء كائنات هذه الفئة وتمريرها بواسطة Aspose.Words إلى طريقة [IWarningCallback.warning(com.aspose.words.WarningInfo)](../../com.aspose.words/iwarningcallback/\#warning-com.aspose.words.WarningInfo).

 **Examples:** 

يوضح كيفية تعيين الخاصية للعثور على أقرب تطابق للخط المفقود من مصادر الخطوط المتاحة.

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


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getDescription()](#getDescription) | يعيد وصف التحذير. |
| [getSource()](#getSource) | يعيد مصدر التحذير. |
| [getWarningType()](#getWarningType) | يعيد نوع التحذير. |
### getDescription() {#getDescription}
```
public String getDescription()
```


يعيد وصف التحذير.

 **Examples:** 

يوضح كيفية تعيين الخاصية للعثور على أقرب تطابق للخط المفقود من مصادر الخطوط المتاحة.

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

يوضح كيفية الحصول على معلومات إضافية حول استبدال الخط.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 WarningInfoCollection callback = new WarningInfoCollection();
 doc.setWarningCallback(callback);

 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Arial", "Arvo", "Slab");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.SubstitutionWarnings.pdf");

 FontSubstitutionWarningInfo warningInfo = (FontSubstitutionWarningInfo)callback.get(0);
 Assert.assertEquals(WarningSource.LAYOUT, warningInfo.getSource());
 Assert.assertEquals(WarningType.FONT_SUBSTITUTION, warningInfo.getWarningType());
 Assert.assertEquals(FontSubstitutionReason.TABLE_SUBSTITUTION_RULE, warningInfo.getReason());
 Assert.assertEquals("Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo.getDescription());
 Assert.assertTrue(warningInfo.getRequestedBold());
 Assert.assertFalse(warningInfo.getRequestedItalic());
 Assert.assertEquals("Arial", warningInfo.getRequestedFamilyName());
 
```

**Returns:**
java.lang.String - وصف التحذير.
### getSource() {#getSource}
```
public int getSource()
```


يعيد مصدر التحذير.

 **Examples:** 

يوضح كيفية التعامل مع مصدر التحذير.

```

 Document doc = new Document(getMyDir() + "Emphases markdown warning.docx");

 WarningInfoCollection warnings = new WarningInfoCollection();
 doc.setWarningCallback(warnings);
 doc.save(getArtifactsDir() + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

 for (WarningInfo warningInfo : warnings) {
     if (warningInfo.getSource() == WarningSource.MARKDOWN)
         Assert.assertEquals("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.getDescription());
 }
 
```

يوضح كيفية الحصول على معلومات إضافية حول استبدال الخط.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 WarningInfoCollection callback = new WarningInfoCollection();
 doc.setWarningCallback(callback);

 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Arial", "Arvo", "Slab");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.SubstitutionWarnings.pdf");

 FontSubstitutionWarningInfo warningInfo = (FontSubstitutionWarningInfo)callback.get(0);
 Assert.assertEquals(WarningSource.LAYOUT, warningInfo.getSource());
 Assert.assertEquals(WarningType.FONT_SUBSTITUTION, warningInfo.getWarningType());
 Assert.assertEquals(FontSubstitutionReason.TABLE_SUBSTITUTION_RULE, warningInfo.getReason());
 Assert.assertEquals("Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo.getDescription());
 Assert.assertTrue(warningInfo.getRequestedBold());
 Assert.assertFalse(warningInfo.getRequestedItalic());
 Assert.assertEquals("Arial", warningInfo.getRequestedFamilyName());
 
```

**Returns:**
int - مصدر التحذير. القيمة المرجعة هي واحدة من ثوابت [WarningSource](../../com.aspose.words/warningsource/).
### getWarningType() {#getWarningType}
```
public int getWarningType()
```


يعيد نوع التحذير.

 **Examples:** 

يوضح كيفية تعيين الخاصية للعثور على أقرب تطابق للخط المفقود من مصادر الخطوط المتاحة.

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

يوضح كيفية الحصول على معلومات إضافية حول استبدال الخط.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 WarningInfoCollection callback = new WarningInfoCollection();
 doc.setWarningCallback(callback);

 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Arial", "Arvo", "Slab");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.SubstitutionWarnings.pdf");

 FontSubstitutionWarningInfo warningInfo = (FontSubstitutionWarningInfo)callback.get(0);
 Assert.assertEquals(WarningSource.LAYOUT, warningInfo.getSource());
 Assert.assertEquals(WarningType.FONT_SUBSTITUTION, warningInfo.getWarningType());
 Assert.assertEquals(FontSubstitutionReason.TABLE_SUBSTITUTION_RULE, warningInfo.getReason());
 Assert.assertEquals("Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo.getDescription());
 Assert.assertTrue(warningInfo.getRequestedBold());
 Assert.assertFalse(warningInfo.getRequestedItalic());
 Assert.assertEquals("Arial", warningInfo.getRequestedFamilyName());
 
```

**Returns:**
int - نوع التحذير. القيمة المرجعة هي تركيبة بتية من ثوابت [WarningType](../../com.aspose.words/warningtype/).
