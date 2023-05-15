---
title: IWarningCallback
linktitle: IWarningCallback
second_title: Aspose.Words for Java
description: Implement this interface if you want to have your own custom method called to capture loss of fidelity warnings that can occur during document loading or saving in Java.
type: docs
weight: 682
url: /java/com.aspose.words/iwarningcallback/
---
```
public interface IWarningCallback
```

Implement this interface if you want to have your own custom method called to capture loss of fidelity warnings that can occur during document loading or saving.

 **Examples:** 

Shows how to use the IWarningCallback interface to monitor font substitution warnings.

```

 public void substitutionWarning() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.getFont().setName("Times New Roman");
     builder.writeln("Hello world!");

     FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
     doc.setWarningCallback(callback);

     // Store the current collection of font sources, which will be the default font source for every document
     // for which we do not specify a different font source.
     FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

     // For testing purposes, we will set Aspose.Words to look for fonts only in a folder that does not exist.
     FontSettings.getDefaultInstance().setFontsFolder("", false);

     // When rendering the document, there will be no place to find the "Times New Roman" font.
     // This will cause a font substitution warning, which our callback will detect.
     doc.save(getArtifactsDir() + "FontSettings.SubstitutionWarning.pdf");

     FontSettings.getDefaultInstance().setFontsSources(originalFontSources);

     Assert.assertTrue(callback.FontSubstitutionWarnings.get(0).getWarningType() == WarningType.FONT_SUBSTITUTION);
     Assert.assertTrue(callback.FontSubstitutionWarnings.get(0).getDescription()
             .equals("Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
 }

 private static class FontSubstitutionWarningCollector implements IWarningCallback {
     /// 
     /// Called every time a warning occurs during loading/saving.
     /// 
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
             FontSubstitutionWarnings.warning(info);
     }

     public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
 }
 
```

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```

 public void enableFontSubstitution() throws Exception {
     // Open a document that contains text formatted with a font that does not exist in any of our font sources.
     Document doc = new Document(getMyDir() + "Missing font.docx");

     // Assign a callback for handling font substitution warnings.
     HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
     doc.setWarningCallback(substitutionWarningHandler);

     // Set a default font name and enable font substitution.
     FontSettings fontSettings = new FontSettings();
     fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
     fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

     // We will get a font substitution warning if we save a document with a missing font.
     doc.setFontSettings(fontSettings);
     doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

     Iterator warnings = substitutionWarningHandler.FontWarnings.iterator();

     while (warnings.hasNext())
         System.out.println(warnings.next().getDescription());

     // We can also verify warnings in the collection and clear them.
     Assert.assertEquals(WarningSource.LAYOUT, substitutionWarningHandler.FontWarnings.get(0).getSource());
     Assert.assertEquals("Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
             substitutionWarningHandler.FontWarnings.get(0).getDescription());

     substitutionWarningHandler.FontWarnings.clear();

     Assert.assertTrue(substitutionWarningHandler.FontWarnings.getCount() == 0);
 }

 public static class HandleDocumentSubstitutionWarnings implements IWarningCallback {
     /// 
     /// Called every time a warning occurs during loading/saving.
     /// 
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
             FontWarnings.warning(info);
     }

     public WarningInfoCollection FontWarnings = new WarningInfoCollection();
 }
 
```
## Methods

| Method | Description |
| --- | --- |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo) | Aspose.Words invokes this method when it encounters some issue during document loading or saving that might result in loss of formatting or data fidelity. |
### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo}
```
public abstract void warning(WarningInfo info)
```


Aspose.Words invokes this method when it encounters some issue during document loading or saving that might result in loss of formatting or data fidelity.

 **Examples:** 

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```

 public void enableFontSubstitution() throws Exception {
     // Open a document that contains text formatted with a font that does not exist in any of our font sources.
     Document doc = new Document(getMyDir() + "Missing font.docx");

     // Assign a callback for handling font substitution warnings.
     HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
     doc.setWarningCallback(substitutionWarningHandler);

     // Set a default font name and enable font substitution.
     FontSettings fontSettings = new FontSettings();
     fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
     fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

     // We will get a font substitution warning if we save a document with a missing font.
     doc.setFontSettings(fontSettings);
     doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

     Iterator warnings = substitutionWarningHandler.FontWarnings.iterator();

     while (warnings.hasNext())
         System.out.println(warnings.next().getDescription());

     // We can also verify warnings in the collection and clear them.
     Assert.assertEquals(WarningSource.LAYOUT, substitutionWarningHandler.FontWarnings.get(0).getSource());
     Assert.assertEquals("Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
             substitutionWarningHandler.FontWarnings.get(0).getDescription());

     substitutionWarningHandler.FontWarnings.clear();

     Assert.assertTrue(substitutionWarningHandler.FontWarnings.getCount() == 0);
 }

 public static class HandleDocumentSubstitutionWarnings implements IWarningCallback {
     /// 
     /// Called every time a warning occurs during loading/saving.
     /// 
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
             FontWarnings.warning(info);
     }

     public WarningInfoCollection FontWarnings = new WarningInfoCollection();
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo/) |  |

