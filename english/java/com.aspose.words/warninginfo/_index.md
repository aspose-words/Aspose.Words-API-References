---
title: WarningInfo
linktitle: WarningInfo
second_title: Aspose.Words for Java
description: Contains information about a warning that Aspose.Words issued during document loading or saving in Java.
type: docs
weight: 706
url: /java/com.aspose.words/warninginfo/
---

**Inheritance:**
java.lang.Object
```
public class WarningInfo
```

Contains information about a warning that Aspose.Words issued during document loading or saving.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.

 **Remarks:** 

You do not create instances of this class. Objects of this class are created and passed by Aspose.Words to the [IWarningCallback.warning(com.aspose.words.WarningInfo)](../../com.aspose.words/iwarningcallback/\#warning-com.aspose.words.WarningInfo) method.

 **Examples:** 

Shows how to set the property for finding the closest match for a missing font from the available font sources.

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
## Methods

| Method | Description |
| --- | --- |
| [getDescription()](#getDescription) | Returns the description of the warning. |
| [getSource()](#getSource) | Returns the source of the warning. |
| [getWarningType()](#getWarningType) | Returns the type of the warning. |
### getDescription() {#getDescription}
```
public String getDescription()
```


Returns the description of the warning.

 **Examples:** 

Shows how to set the property for finding the closest match for a missing font from the available font sources.

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
java.lang.String - The description of the warning.
### getSource() {#getSource}
```
public int getSource()
```


Returns the source of the warning.

 **Examples:** 

Shows how to work with the warning source.

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

**Returns:**
int - The source of the warning. The returned value is one of [WarningSource](../../com.aspose.words/warningsource/) constants.
### getWarningType() {#getWarningType}
```
public int getWarningType()
```


Returns the type of the warning.

 **Examples:** 

Shows how to set the property for finding the closest match for a missing font from the available font sources.

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
int - The type of the warning. The returned value is a bitwise combination of [WarningType](../../com.aspose.words/warningtype/) constants.
