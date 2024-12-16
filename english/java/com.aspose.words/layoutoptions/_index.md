---
title: LayoutOptions
linktitle: LayoutOptions
second_title: Aspose.Words for Java
description: Holds the options that allow controlling the document layout process in Java.
type: docs
weight: 408
url: /java/com.aspose.words/layoutoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class LayoutOptions implements Cloneable
```

Holds the options that allow controlling the document layout process.

To learn more, visit the [ Converting to Fixed-page Format ][Converting to Fixed-page Format] documentation article.

 **Remarks:** 

You do not create instances of this class directly. Use the [Document.getLayoutOptions()](../../com.aspose.words/document/\#getLayoutOptions) property to access layout options for this document.

Note that after changing any of the options present in this class, [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) method should be called in order for the changed options to be applied to the layout.

 **Examples:** 

Shows how to hide text in a rendered output document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // Insert hidden text, then specify whether we wish to omit it from a rendered document.
 builder.writeln("This text is not hidden.");
 builder.getFont().setHidden(true);
 builder.writeln("This text is hidden.");

 doc.getLayoutOptions().setShowHiddenText(showHiddenText);

 doc.save(getArtifactsDir() + "Document.LayoutOptionsHiddenText.pdf");
 
```

Shows how to show paragraph marks in a rendered output document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // Add some paragraphs, then enable paragraph marks to show the ends of paragraphs
 // with a pilcrow (¶) symbol when we render the document.
 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 doc.getLayoutOptions().setShowParagraphMarks(showParagraphMarks);

 doc.save(getArtifactsDir() + "Document.LayoutOptionsParagraphMarks.pdf");
 
```

Shows how to alter the appearance of revisions in a rendered output document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Document.LayoutOptionsRevisions.pdf");
 
```


[Converting to Fixed-page Format]: https://docs.aspose.com/words/java/converting-to-fixed-page-format/
## Methods

| Method | Description |
| --- | --- |
| [getCallback()](#getCallback) | Gets [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback/) implementation used by page layout model. |
| [getCommentDisplayMode()](#getCommentDisplayMode) | Gets the way comments are rendered. |
| [getContinuousSectionPageNumberingRestart()](#getContinuousSectionPageNumberingRestart) | Gets the mode of behavior for computing page numbers when a continuous section restarts the page numbering. |
| [getIgnorePrinterMetrics()](#getIgnorePrinterMetrics) | Gets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. |
| [getKeepOriginalFontMetrics()](#getKeepOriginalFontMetrics) | Gets an indication of whether the original font metrics should be used after font substitution. |
| [getRevisionOptions()](#getRevisionOptions) | Gets revision options. |
| [getShowHiddenText()](#getShowHiddenText) | Gets indication of whether hidden text in the document is rendered. |
| [getShowParagraphMarks()](#getShowParagraphMarks) | Gets indication of whether paragraph marks are rendered. |
| [getTextShaperFactory()](#getTextShaperFactory) | Gets [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) implementation used for Advanced Typography rendering features. |
| [setCallback(IPageLayoutCallback value)](#setCallback-com.aspose.words.IPageLayoutCallback) | Sets [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback/) implementation used by page layout model. |
| [setCommentDisplayMode(int value)](#setCommentDisplayMode-int) | Sets the way comments are rendered. |
| [setContinuousSectionPageNumberingRestart(int value)](#setContinuousSectionPageNumberingRestart-int) | Sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering. |
| [setIgnorePrinterMetrics(boolean value)](#setIgnorePrinterMetrics-boolean) | Sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. |
| [setKeepOriginalFontMetrics(boolean value)](#setKeepOriginalFontMetrics-boolean) | Sets an indication of whether the original font metrics should be used after font substitution. |
| [setShowHiddenText(boolean value)](#setShowHiddenText-boolean) | Sets indication of whether hidden text in the document is rendered. |
| [setShowParagraphMarks(boolean value)](#setShowParagraphMarks-boolean) | Sets indication of whether paragraph marks are rendered. |
| [setTextShaperFactory(ITextShaperFactory value)](#setTextShaperFactory-com.aspose.words.ITextShaperFactory) | Sets [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) implementation used for Advanced Typography rendering features. |
### getCallback() {#getCallback}
```
public IPageLayoutCallback getCallback()
```


Gets [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback/) implementation used by page layout model.

 **Examples:** 

Shows how to track layout changes with a layout callback.

```

 public void pageLayoutCallback() throws Exception {
     Document doc = new Document();
     doc.getBuiltInDocumentProperties().setTitle("My Document");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world!");

     doc.getLayoutOptions().setCallback(new RenderPageLayoutCallback());
     doc.updatePageLayout();

     doc.save(getArtifactsDir() + "Layout.PageLayoutCallback.pdf");
 }

 /// 
 /// Notifies us when we save the document to a fixed page format
 /// and renders a page that we perform a page reflow on to an image in the local file system.
 /// 
 private static class RenderPageLayoutCallback implements IPageLayoutCallback {
     public void notify(PageLayoutCallbackArgs a) throws Exception {
         switch (a.getEvent()) {
             case PageLayoutEvent.PART_REFLOW_FINISHED:
                 notifyPartFinished(a);
                 break;
             case PageLayoutEvent.CONVERSION_FINISHED:
                 notifyConversionFinished(a);
                 break;
         }
     }

     private void notifyPartFinished(PageLayoutCallbackArgs a) throws Exception {
         System.out.println(MessageFormat.format("Part at page {0} reflow.", a.getPageIndex() + 1));
         renderPage(a, a.getPageIndex());
     }

     private void notifyConversionFinished(PageLayoutCallbackArgs a) {
         System.out.println(MessageFormat.format("Document \"{0}\" converted to page format.", a.getDocument().getBuiltInDocumentProperties().getTitle()));
     }

     private void renderPage(PageLayoutCallbackArgs a, int pageIndex) throws Exception {
         ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
         {
             saveOptions.setPageSet(new PageSet(pageIndex));
         }

         try (FileOutputStream stream = new FileOutputStream(getArtifactsDir() + MessageFormat.format("PageLayoutCallback.page-{0} {1}.png", pageIndex + 1, ++mNum))) {
             a.getDocument().save(stream, saveOptions);
         }
     }

     private int mNum;
 }
 
```

**Returns:**
[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback/) - [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback/) implementation used by page layout model.
### getCommentDisplayMode() {#getCommentDisplayMode}
```
public int getCommentDisplayMode()
```


Gets the way comments are rendered. Default value is [CommentDisplayMode.SHOW\_IN\_BALLOONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-BALLOONS).

 **Remarks:** 

Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS).

 **Examples:** 

Shows how to show comments when saving a document to a rendered format.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");

 Comment comment = new Comment(doc, "John Doe", "J.D.", new Date());
 comment.setText("My comment.");
 builder.getCurrentParagraph().appendChild(comment);

 // ShowInAnnotations is only available in Pdf1.7 and Pdf1.5 formats.
 // In other formats, it will work similarly to Hide.
 doc.getLayoutOptions().setCommentDisplayMode(CommentDisplayMode.SHOW_IN_ANNOTATIONS);

 doc.save(getArtifactsDir() + "Document.ShowCommentsInAnnotations.pdf");

 // Note that it's required to rebuild the document page layout (via Document.UpdatePageLayout() method)
 // after changing the Document.LayoutOptions values.
 doc.getLayoutOptions().setCommentDisplayMode(CommentDisplayMode.SHOW_IN_BALLOONS);
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.ShowCommentsInBalloons.pdf");
 
```

**Returns:**
int - The way comments are rendered. The returned value is one of [CommentDisplayMode](../../com.aspose.words/commentdisplaymode/) constants.
### getContinuousSectionPageNumberingRestart() {#getContinuousSectionPageNumberingRestart}
```
public int getContinuousSectionPageNumberingRestart()
```


Gets the mode of behavior for computing page numbers when a continuous section restarts the page numbering.

 **Remarks:** 

The default value is [ContinuousSectionRestart.ALWAYS](../../com.aspose.words/continuoussectionrestart/\#ALWAYS). It matches the behavior of MS Word 2019 which was the latest version at the moment the option was introduced. Older page numbering logic demonstrated by MS Word 2016 is available via this option. Please [ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart/) for the behavior description.

 **Examples:** 

Shows how to control page numbering in a continuous section.

```

 Document doc = new Document(getMyDir() + "Continuous section page numbering.docx");

 // By default Aspose.Words behavior matches the Microsoft Word 2019.
 // If you need old Aspose.Words behavior, repetitive Microsoft Word 2016, use 'ContinuousSectionRestart.FromNewPageOnly'.
 // Page numbering restarts only if there is no other content before the section on the page where the section starts,
 // because of that the numbering will reset to 2 from the second page.
 doc.getLayoutOptions().setContinuousSectionPageNumberingRestart(ContinuousSectionRestart.FROM_NEW_PAGE_ONLY);
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Layout.RestartPageNumberingInContinuousSection.pdf");
 
```

**Returns:**
int - The mode of behavior for computing page numbers when a continuous section restarts the page numbering. The returned value is one of [ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart/) constants.
### getIgnorePrinterMetrics() {#getIgnorePrinterMetrics}
```
public boolean getIgnorePrinterMetrics()
```


Gets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is  true .

 **Examples:** 

Shows how to ignore 'Use printer metrics to lay out document' option.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 doc.getLayoutOptions().setIgnorePrinterMetrics(false);

 doc.save(getArtifactsDir() + "Document.IgnorePrinterMetrics.docx");
 
```

**Returns:**
boolean - Indication of whether the "Use printer metrics to lay out document" compatibility option is ignored.
### getKeepOriginalFontMetrics() {#getKeepOriginalFontMetrics}
```
public boolean getKeepOriginalFontMetrics()
```


Gets an indication of whether the original font metrics should be used after font substitution. Default is  true .

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

     // Original font metrics should be used after font substitution.
     doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

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

**Returns:**
boolean - An indication of whether the original font metrics should be used after font substitution.
### getRevisionOptions() {#getRevisionOptions}
```
public RevisionOptions getRevisionOptions()
```


Gets revision options.

 **Examples:** 

Shows how to alter the appearance of revisions in a rendered output document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Document.LayoutOptionsRevisions.pdf");
 
```

**Returns:**
[RevisionOptions](../../com.aspose.words/revisionoptions/) - Revision options.
### getShowHiddenText() {#getShowHiddenText}
```
public boolean getShowHiddenText()
```


Gets indication of whether hidden text in the document is rendered. Default is  false .

 **Remarks:** 

This property affects all hidden content, not just text.

 **Examples:** 

Shows how to hide text in a rendered output document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // Insert hidden text, then specify whether we wish to omit it from a rendered document.
 builder.writeln("This text is not hidden.");
 builder.getFont().setHidden(true);
 builder.writeln("This text is hidden.");

 doc.getLayoutOptions().setShowHiddenText(showHiddenText);

 doc.save(getArtifactsDir() + "Document.LayoutOptionsHiddenText.pdf");
 
```

**Returns:**
boolean - Indication of whether hidden text in the document is rendered.
### getShowParagraphMarks() {#getShowParagraphMarks}
```
public boolean getShowParagraphMarks()
```


Gets indication of whether paragraph marks are rendered. Default is  false .

 **Examples:** 

Shows how to show paragraph marks in a rendered output document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // Add some paragraphs, then enable paragraph marks to show the ends of paragraphs
 // with a pilcrow (¶) symbol when we render the document.
 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 doc.getLayoutOptions().setShowParagraphMarks(showParagraphMarks);

 doc.save(getArtifactsDir() + "Document.LayoutOptionsParagraphMarks.pdf");
 
```

**Returns:**
boolean - Indication of whether paragraph marks are rendered.
### getTextShaperFactory() {#getTextShaperFactory}
```
public ITextShaperFactory getTextShaperFactory()
```


Gets [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) implementation used for Advanced Typography rendering features.

 **Examples:** 

Shows how to support OpenType features using the HarfBuzz text shaping engine.

```

 Document doc = new Document(getMyDir() + "OpenType text shaping.docx");

 // Aspose.Words can use externally provided text shaper objects,
 // which represent fonts and compute shaping information for text.
 // A text shaper factory is necessary for documents that use multiple fonts.
 // When the text shaper factory set, the layout uses OpenType features.
 // An Instance property returns a static BasicTextShaperCache object wrapping HarfBuzzTextShaperFactory.
 doc.getLayoutOptions().setTextShaperFactory(HarfBuzzTextShaperFactory.getInstance());

 // Currently, text shaping is performing when exporting to PDF or XPS formats.
 doc.save(getArtifactsDir() + "Document.OpenType.pdf");
 
```

**Returns:**
[ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) - [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) implementation used for Advanced Typography rendering features.
### setCallback(IPageLayoutCallback value) {#setCallback-com.aspose.words.IPageLayoutCallback}
```
public void setCallback(IPageLayoutCallback value)
```


Sets [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback/) implementation used by page layout model.

 **Examples:** 

Shows how to track layout changes with a layout callback.

```

 public void pageLayoutCallback() throws Exception {
     Document doc = new Document();
     doc.getBuiltInDocumentProperties().setTitle("My Document");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world!");

     doc.getLayoutOptions().setCallback(new RenderPageLayoutCallback());
     doc.updatePageLayout();

     doc.save(getArtifactsDir() + "Layout.PageLayoutCallback.pdf");
 }

 /// 
 /// Notifies us when we save the document to a fixed page format
 /// and renders a page that we perform a page reflow on to an image in the local file system.
 /// 
 private static class RenderPageLayoutCallback implements IPageLayoutCallback {
     public void notify(PageLayoutCallbackArgs a) throws Exception {
         switch (a.getEvent()) {
             case PageLayoutEvent.PART_REFLOW_FINISHED:
                 notifyPartFinished(a);
                 break;
             case PageLayoutEvent.CONVERSION_FINISHED:
                 notifyConversionFinished(a);
                 break;
         }
     }

     private void notifyPartFinished(PageLayoutCallbackArgs a) throws Exception {
         System.out.println(MessageFormat.format("Part at page {0} reflow.", a.getPageIndex() + 1));
         renderPage(a, a.getPageIndex());
     }

     private void notifyConversionFinished(PageLayoutCallbackArgs a) {
         System.out.println(MessageFormat.format("Document \"{0}\" converted to page format.", a.getDocument().getBuiltInDocumentProperties().getTitle()));
     }

     private void renderPage(PageLayoutCallbackArgs a, int pageIndex) throws Exception {
         ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
         {
             saveOptions.setPageSet(new PageSet(pageIndex));
         }

         try (FileOutputStream stream = new FileOutputStream(getArtifactsDir() + MessageFormat.format("PageLayoutCallback.page-{0} {1}.png", pageIndex + 1, ++mNum))) {
             a.getDocument().save(stream, saveOptions);
         }
     }

     private int mNum;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback/) | [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback/) implementation used by page layout model. |

### setCommentDisplayMode(int value) {#setCommentDisplayMode-int}
```
public void setCommentDisplayMode(int value)
```


Sets the way comments are rendered. Default value is [CommentDisplayMode.SHOW\_IN\_BALLOONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-BALLOONS).

 **Remarks:** 

Note that revisions are not rendered in balloons for [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS).

 **Examples:** 

Shows how to show comments when saving a document to a rendered format.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");

 Comment comment = new Comment(doc, "John Doe", "J.D.", new Date());
 comment.setText("My comment.");
 builder.getCurrentParagraph().appendChild(comment);

 // ShowInAnnotations is only available in Pdf1.7 and Pdf1.5 formats.
 // In other formats, it will work similarly to Hide.
 doc.getLayoutOptions().setCommentDisplayMode(CommentDisplayMode.SHOW_IN_ANNOTATIONS);

 doc.save(getArtifactsDir() + "Document.ShowCommentsInAnnotations.pdf");

 // Note that it's required to rebuild the document page layout (via Document.UpdatePageLayout() method)
 // after changing the Document.LayoutOptions values.
 doc.getLayoutOptions().setCommentDisplayMode(CommentDisplayMode.SHOW_IN_BALLOONS);
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.ShowCommentsInBalloons.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The way comments are rendered. The value must be one of [CommentDisplayMode](../../com.aspose.words/commentdisplaymode/) constants. |

### setContinuousSectionPageNumberingRestart(int value) {#setContinuousSectionPageNumberingRestart-int}
```
public void setContinuousSectionPageNumberingRestart(int value)
```


Sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering.

 **Remarks:** 

The default value is [ContinuousSectionRestart.ALWAYS](../../com.aspose.words/continuoussectionrestart/\#ALWAYS). It matches the behavior of MS Word 2019 which was the latest version at the moment the option was introduced. Older page numbering logic demonstrated by MS Word 2016 is available via this option. Please [ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart/) for the behavior description.

 **Examples:** 

Shows how to control page numbering in a continuous section.

```

 Document doc = new Document(getMyDir() + "Continuous section page numbering.docx");

 // By default Aspose.Words behavior matches the Microsoft Word 2019.
 // If you need old Aspose.Words behavior, repetitive Microsoft Word 2016, use 'ContinuousSectionRestart.FromNewPageOnly'.
 // Page numbering restarts only if there is no other content before the section on the page where the section starts,
 // because of that the numbering will reset to 2 from the second page.
 doc.getLayoutOptions().setContinuousSectionPageNumberingRestart(ContinuousSectionRestart.FROM_NEW_PAGE_ONLY);
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Layout.RestartPageNumberingInContinuousSection.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The mode of behavior for computing page numbers when a continuous section restarts the page numbering. The value must be one of [ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart/) constants. |

### setIgnorePrinterMetrics(boolean value) {#setIgnorePrinterMetrics-boolean}
```
public void setIgnorePrinterMetrics(boolean value)
```


Sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is  true .

 **Examples:** 

Shows how to ignore 'Use printer metrics to lay out document' option.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 doc.getLayoutOptions().setIgnorePrinterMetrics(false);

 doc.save(getArtifactsDir() + "Document.IgnorePrinterMetrics.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. |

### setKeepOriginalFontMetrics(boolean value) {#setKeepOriginalFontMetrics-boolean}
```
public void setKeepOriginalFontMetrics(boolean value)
```


Sets an indication of whether the original font metrics should be used after font substitution. Default is  true .

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

     // Original font metrics should be used after font substitution.
     doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

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
| value | boolean | An indication of whether the original font metrics should be used after font substitution. |

### setShowHiddenText(boolean value) {#setShowHiddenText-boolean}
```
public void setShowHiddenText(boolean value)
```


Sets indication of whether hidden text in the document is rendered. Default is  false .

 **Remarks:** 

This property affects all hidden content, not just text.

 **Examples:** 

Shows how to hide text in a rendered output document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // Insert hidden text, then specify whether we wish to omit it from a rendered document.
 builder.writeln("This text is not hidden.");
 builder.getFont().setHidden(true);
 builder.writeln("This text is hidden.");

 doc.getLayoutOptions().setShowHiddenText(showHiddenText);

 doc.save(getArtifactsDir() + "Document.LayoutOptionsHiddenText.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Indication of whether hidden text in the document is rendered. |

### setShowParagraphMarks(boolean value) {#setShowParagraphMarks-boolean}
```
public void setShowParagraphMarks(boolean value)
```


Sets indication of whether paragraph marks are rendered. Default is  false .

 **Examples:** 

Shows how to show paragraph marks in a rendered output document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // Add some paragraphs, then enable paragraph marks to show the ends of paragraphs
 // with a pilcrow (¶) symbol when we render the document.
 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 doc.getLayoutOptions().setShowParagraphMarks(showParagraphMarks);

 doc.save(getArtifactsDir() + "Document.LayoutOptionsParagraphMarks.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Indication of whether paragraph marks are rendered. |

### setTextShaperFactory(ITextShaperFactory value) {#setTextShaperFactory-com.aspose.words.ITextShaperFactory}
```
public void setTextShaperFactory(ITextShaperFactory value)
```


Sets [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) implementation used for Advanced Typography rendering features.

 **Examples:** 

Shows how to support OpenType features using the HarfBuzz text shaping engine.

```

 Document doc = new Document(getMyDir() + "OpenType text shaping.docx");

 // Aspose.Words can use externally provided text shaper objects,
 // which represent fonts and compute shaping information for text.
 // A text shaper factory is necessary for documents that use multiple fonts.
 // When the text shaper factory set, the layout uses OpenType features.
 // An Instance property returns a static BasicTextShaperCache object wrapping HarfBuzzTextShaperFactory.
 doc.getLayoutOptions().setTextShaperFactory(HarfBuzzTextShaperFactory.getInstance());

 // Currently, text shaping is performing when exporting to PDF or XPS formats.
 doc.save(getArtifactsDir() + "Document.OpenType.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) implementation used for Advanced Typography rendering features. |

