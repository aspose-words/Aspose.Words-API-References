---
title: FieldOptions
linktitle: FieldOptions
second_title: Aspose.Words for Java
description: Represents options to control field handling in a document in Java.
type: docs
weight: 270
url: /java/com.aspose.words/fieldoptions/
---

**Inheritance:**
java.lang.Object
```
public class FieldOptions
```

Represents options to control field handling in a document.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Methods

| Method | Description |
| --- | --- |
| [getBarcodeGenerator()](#getBarcodeGenerator) | Gets or set custom barcode generator. |
| [getBibliographyStylesProvider()](#getBibliographyStylesProvider) | Gets a provider that returns a bibliography style for the [FieldBibliography](../../com.aspose.words/fieldbibliography/) and [FieldCitation](../../com.aspose.words/fieldcitation/) fields. |
| [getBuiltInTemplatesPaths()](#getBuiltInTemplatesPaths) | Gets paths of MS Word built-in templates. |
| [getComparisonExpressionEvaluator()](#getComparisonExpressionEvaluator) | Gets the field comparison expressions evaluator. |
| [getCurrentUser()](#getCurrentUser) | Gets the current user information. |
| [getCustomTocStyleSeparator()](#getCustomTocStyleSeparator) | Gets custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc/) field. |
| [getDefaultDocumentAuthor()](#getDefaultDocumentAuthor) | Gets default document author's name. |
| [getFieldDatabaseProvider()](#getFieldDatabaseProvider) | Gets a provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase/) field. |
| [getFieldIndexFormat()](#getFieldIndexFormat) | Gets a [getFieldIndexFormat()](../../com.aspose.words/fieldoptions/\#getFieldIndexFormat) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions/\#setFieldIndexFormat-int) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex/) fields in the document. |
| [getFieldUpdateCultureProvider()](#getFieldUpdateCultureProvider) | Gets a provider that returns a culture object specific for each particular field. |
| [getFieldUpdateCultureSource()](#getFieldUpdateCultureSource) | Specifies what culture to use to format the field result. |
| [getFieldUpdatingCallback()](#getFieldUpdatingCallback) | Gets [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback/) implementation |
| [getFieldUpdatingProgressCallback()](#getFieldUpdatingProgressCallback) | Gets [IFieldUpdatingProgressCallback](../../com.aspose.words/ifieldupdatingprogresscallback/) implementation. |
| [getFileName()](#getFileName) | Gets the file name of the document. |
| [getLegacyNumberFormat()](#getLegacyNumberFormat) | Gets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not. |
| [getPreProcessCulture()](#getPreProcessCulture) | Gets the culture to preprocess field values. |
| [getResultFormatter()](#getResultFormatter) | Allows to control how the field result is formatted. |
| [getTemplateName()](#getTemplateName) | Gets the file name of the template used by the document. |
| [getToaCategories()](#getToaCategories) | Gets the table of authorities categories. |
| [getUseInvariantCultureNumberFormat()](#getUseInvariantCultureNumberFormat) | Gets the value indicating that number format is parsed using invariant culture or not |
| [getUserPromptRespondent()](#getUserPromptRespondent) | Gets the respondent to user prompts during field update. |
| [isBidiTextSupportedOnUpdate()](#isBidiTextSupportedOnUpdate) | Gets the value indicating whether bidirectional text is fully supported during field update or not. |
| [isBidiTextSupportedOnUpdate(boolean value)](#isBidiTextSupportedOnUpdate-boolean) | Sets the value indicating whether bidirectional text is fully supported during field update or not. |
| [setBarcodeGenerator(IBarcodeGenerator value)](#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator) | Gets or set custom barcode generator. |
| [setBibliographyStylesProvider(IBibliographyStylesProvider value)](#setBibliographyStylesProvider-com.aspose.words.IBibliographyStylesProvider) | Sets a provider that returns a bibliography style for the [FieldBibliography](../../com.aspose.words/fieldbibliography/) and [FieldCitation](../../com.aspose.words/fieldcitation/) fields. |
| [setBuiltInTemplatesPaths(String[] value)](#setBuiltInTemplatesPaths-java.lang.String) | Sets paths of MS Word built-in templates. |
| [setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value)](#setComparisonExpressionEvaluator-com.aspose.words.IComparisonExpressionEvaluator) | Sets the field comparison expressions evaluator. |
| [setCurrentUser(UserInformation value)](#setCurrentUser-com.aspose.words.UserInformation) | Sets the current user information. |
| [setCustomTocStyleSeparator(String value)](#setCustomTocStyleSeparator-java.lang.String) | Sets custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc/) field. |
| [setDefaultDocumentAuthor(String value)](#setDefaultDocumentAuthor-java.lang.String) | Sets default document author's name. |
| [setFieldDatabaseProvider(IFieldDatabaseProvider value)](#setFieldDatabaseProvider-com.aspose.words.IFieldDatabaseProvider) | Sets a provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase/) field. |
| [setFieldIndexFormat(int value)](#setFieldIndexFormat-int) | Sets a [getFieldIndexFormat()](../../com.aspose.words/fieldoptions/\#getFieldIndexFormat) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions/\#setFieldIndexFormat-int) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex/) fields in the document. |
| [setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value)](#setFieldUpdateCultureProvider-com.aspose.words.IFieldUpdateCultureProvider) | Sets a provider that returns a culture object specific for each particular field. |
| [setFieldUpdateCultureSource(int value)](#setFieldUpdateCultureSource-int) | Specifies what culture to use to format the field result. |
| [setFieldUpdatingCallback(IFieldUpdatingCallback value)](#setFieldUpdatingCallback-com.aspose.words.IFieldUpdatingCallback) | Sets [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback/) implementation |
| [setFieldUpdatingProgressCallback(IFieldUpdatingProgressCallback value)](#setFieldUpdatingProgressCallback-com.aspose.words.IFieldUpdatingProgressCallback) | Sets [IFieldUpdatingProgressCallback](../../com.aspose.words/ifieldupdatingprogresscallback/) implementation. |
| [setFileName(String value)](#setFileName-java.lang.String) | Sets the file name of the document. |
| [setLegacyNumberFormat(boolean value)](#setLegacyNumberFormat-boolean) | Sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not. |
| [setPreProcessCulture(System.Globalization.CultureInfo value)](#setPreProcessCulture-com.aspose.words.net.System.Globalization.CultureInfo) | Sets the culture to preprocess field values. |
| [setResultFormatter(IFieldResultFormatter value)](#setResultFormatter-com.aspose.words.IFieldResultFormatter) | Allows to control how the field result is formatted. |
| [setTemplateName(String value)](#setTemplateName-java.lang.String) | Sets the file name of the template used by the document. |
| [setToaCategories(ToaCategories value)](#setToaCategories-com.aspose.words.ToaCategories) | Sets the table of authorities categories. |
| [setUseInvariantCultureNumberFormat(boolean value)](#setUseInvariantCultureNumberFormat-boolean) | Sets the value indicating that number format is parsed using invariant culture or not |
| [setUserPromptRespondent(IFieldUserPromptRespondent value)](#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent) | Sets the respondent to user prompts during field update. |
### getBarcodeGenerator() {#getBarcodeGenerator}
```
public IBarcodeGenerator getBarcodeGenerator()
```


Gets or set custom barcode generator.

 **Remarks:** 

Custom barcode generator should implement public interface [IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator/).

 **Examples:** 

Shows how to use a barcode generator.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // We can use a custom IBarcodeGenerator implementation to generate barcodes,
 // and then insert them into the document as images.
 doc.getFieldOptions().setBarcodeGenerator(new CustomBarcodeGenerator());

 // Below are four examples of different barcode types that we can create using our generator.
 // For each barcode, we specify a new set of barcode parameters, and then generate the image.
 // Afterwards, we can insert the image into the document, or save it to the local file system.
 // 1 -  QR code:
 BarcodeParameters barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("QR");
     barcodeParameters.setBarcodeValue("ABC123");
     barcodeParameters.setBackgroundColor("0xF8BD69");
     barcodeParameters.setForegroundColor("0xB5413B");
     barcodeParameters.setErrorCorrectionLevel("3");
     barcodeParameters.setScalingFactor("250");
     barcodeParameters.setSymbolHeight("1000");
     barcodeParameters.setSymbolRotation("0");
 }

 BufferedImage img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.QR.jpg"));

 builder.insertImage(img);

 // 2 -  EAN13 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("EAN13");
     barcodeParameters.setBarcodeValue("501234567890");
     barcodeParameters.setDisplayText(true);
     barcodeParameters.setPosCodeStyle("CASE");
     barcodeParameters.setFixCheckDigit(true);
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.EAN13.jpg"));
 builder.insertImage(img);

 // 3 -  CODE39 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("CODE39");
     barcodeParameters.setBarcodeValue("12345ABCDE");
     barcodeParameters.setAddStartStopChar(true);
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.CODE39.jpg"));
 builder.insertImage(img);

 // 4 -  ITF14 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("ITF14");
     barcodeParameters.setBarcodeValue("09312345678907");
     barcodeParameters.setCaseCodeStyle("STD");
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.ITF14.jpg"));
 builder.insertImage(img);

 doc.save(getArtifactsDir() + "FieldOptions.BarcodeGenerator.docx");
 
```

**Returns:**
[IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator/) - Or set custom barcode generator.
### getBibliographyStylesProvider() {#getBibliographyStylesProvider}
```
public IBibliographyStylesProvider getBibliographyStylesProvider()
```


Gets a provider that returns a bibliography style for the [FieldBibliography](../../com.aspose.words/fieldbibliography/) and [FieldCitation](../../com.aspose.words/fieldcitation/) fields.

 **Examples:** 

Shows how to override built-in styles or provide custom one.

```

 public void changeBibliographyStyles() throws Exception
 {
     Document doc = new Document(getMyDir() + "Bibliography.docx");

     // If the document already has a style you can change it with the following code:
     // doc.Bibliography.BibliographyStyle = "Bibliography custom style.xsl";

     doc.getFieldOptions().setBibliographyStylesProvider(new BibliographyStylesProvider());
     doc.updateFields();

     doc.save(getArtifactsDir() + "Field.ChangeBibliographyStyles.docx");
 }

 public static class BibliographyStylesProvider implements IBibliographyStylesProvider
 {
     public FileInputStream getStyle(String styleFileName) throws Exception
     {
         return new FileInputStream(getMyDir() + "Bibliography custom style.xsl");
     }
 }
 
```

**Returns:**
[IBibliographyStylesProvider](../../com.aspose.words/ibibliographystylesprovider/) - A provider that returns a bibliography style for the [FieldBibliography](../../com.aspose.words/fieldbibliography/) and [FieldCitation](../../com.aspose.words/fieldcitation/) fields.
### getBuiltInTemplatesPaths() {#getBuiltInTemplatesPaths}
```
public String[] getBuiltInTemplatesPaths()
```


Gets paths of MS Word built-in templates.

 **Remarks:** 

This property is used by the [FieldAutoText](../../com.aspose.words/fieldautotext/) and [FieldGlossary](../../com.aspose.words/fieldglossary/) fields, if referenced auto text entry is not found in the [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) template.

By default MS Word stores built-in templates in c:\\Users\\\\AppData\\Roaming\\Microsoft\\Document Building Blocks\\1033\\16\\Built-In Building Blocks.dotx and C:\\Users\\\\AppData\\Roaming\\Microsoft\\Templates\\Normal.dotm files.

 **Examples:** 

Shows how to display a building block with AUTOTEXT and GLOSSARY fields.

```

 Document doc = new Document();

 // Create a glossary document and add an AutoText building block to it.
 doc.setGlossaryDocument(new GlossaryDocument());
 BuildingBlock buildingBlock = new BuildingBlock(doc.getGlossaryDocument());
 buildingBlock.setName("MyBlock");
 buildingBlock.setGallery(BuildingBlockGallery.AUTO_TEXT);
 buildingBlock.setCategory("General");
 buildingBlock.setDescription("MyBlock description");
 buildingBlock.setBehavior(BuildingBlockBehavior.PARAGRAPH);
 doc.getGlossaryDocument().appendChild(buildingBlock);

 // Create a source and add it as text to our building block.
 Document buildingBlockSource = new Document();
 DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
 buildingBlockSourceBuilder.writeln("Hello World!");

 Node buildingBlockContent = doc.getGlossaryDocument().importNode(buildingBlockSource.getFirstSection(), true);
 buildingBlock.appendChild(buildingBlockContent);

 // Set a file which contains parts that our document, or its attached template may not contain.
 doc.getFieldOptions().setBuiltInTemplatesPaths(new String[]{getMyDir() + "Busniess brochure.dotx"});

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways to use fields to display the contents of our building block.
 // 1 -  Using an AUTOTEXT field:
 FieldAutoText fieldAutoText = (FieldAutoText) builder.insertField(FieldType.FIELD_AUTO_TEXT, true);
 fieldAutoText.setEntryName("MyBlock");

 Assert.assertEquals(" AUTOTEXT  MyBlock", fieldAutoText.getFieldCode());

 // 2 -  Using a GLOSSARY field:
 FieldGlossary fieldGlossary = (FieldGlossary) builder.insertField(FieldType.FIELD_GLOSSARY, true);
 fieldGlossary.setEntryName("MyBlock");

 Assert.assertEquals(fieldGlossary.getFieldCode(), " GLOSSARY  MyBlock");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.AUTOTEXT.GLOSSARY.dotx");
 
```

**Returns:**
java.lang.String[] - Paths of MS Word built-in templates.
### getComparisonExpressionEvaluator() {#getComparisonExpressionEvaluator}
```
public IComparisonExpressionEvaluator getComparisonExpressionEvaluator()
```


Gets the field comparison expressions evaluator.

 **Examples:** 

Shows how to implement custom evaluation for the IF and COMPARE fields.

```

 public void conditionEvaluationExtensionPoint(String fieldCode, byte comparisonResult, String comparisonError,
                                               String expectedResult) throws Exception {
     final String LEFT = "\"left expression\"";
     final String _OPERATOR = "<>";
     final String RIGHT = "\"right expression\"";

     DocumentBuilder builder = new DocumentBuilder();

     // Field codes that we use in this example:
     // 1.   " IF %s %s %s \"true argument\" \"false argument\" ".
     // 2.   " COMPARE %s %s %s ".
     Field field = builder.insertField(String.format(fieldCode, LEFT, _OPERATOR, RIGHT), null);

     // If the "comparisonResult" is undefined, we create "ComparisonEvaluationResult" with string, instead of bool.
     ComparisonEvaluationResult result = comparisonResult != -1
             ? new ComparisonEvaluationResult(comparisonResult == 1)
             : comparisonError != null ? new ComparisonEvaluationResult(comparisonError) : null;

     ComparisonExpressionEvaluator evaluator = new ComparisonExpressionEvaluator(result);
     builder.getDocument().getFieldOptions().setComparisonExpressionEvaluator(evaluator);

     builder.getDocument().updateFields();

     Assert.assertEquals(expectedResult, field.getResult());
     evaluator.assertInvocationsCount(1).assertInvocationArguments(0, LEFT, _OPERATOR, RIGHT);
 }

 public static Object[][] conditionEvaluationExtensionPointDataProvider() {
     return new Object[][]
             {
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) 1, null, "true argument"},
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) 0, null, "false argument"},
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) -1, "Custom Error", "Custom Error"},
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) -1, null, "true argument"},
                     {" COMPARE %s %s %s ", (byte) 1, null, "1"},
                     {" COMPARE %s %s %s ", (byte) 0, null, "0"},
                     {" COMPARE %s %s %s ", (byte) -1, "Custom Error", "Custom Error"},
                     {" COMPARE %s %s %s ", (byte) -1, null, "1"},
             };
 }

 /// 
 /// Comparison expressions evaluation for the FieldIf and FieldCompare.
 /// 
 private static class ComparisonExpressionEvaluator implements IComparisonExpressionEvaluator {
     public ComparisonExpressionEvaluator(ComparisonEvaluationResult result) {
         mResult = result;
     }

     public ComparisonEvaluationResult evaluate(Field field, ComparisonExpression expression) {
         mInvocations.add(new String[]
                 {
                         expression.getLeftExpression(),
                         expression.getComparisonOperator(),
                         expression.getRightExpression()
                 });

         return mResult;
     }

     public ComparisonExpressionEvaluator assertInvocationsCount(int expected) {
         Assert.assertEquals(expected, mInvocations.size());
         return this;
     }

     public ComparisonExpressionEvaluator assertInvocationArguments(
             int invocationIndex,
             String expectedLeftExpression,
             String expectedComparisonOperator,
             String expectedRightExpression) {
         String[] arguments = mInvocations.get(invocationIndex);

         Assert.assertEquals(expectedLeftExpression, arguments[0]);
         Assert.assertEquals(expectedComparisonOperator, arguments[1]);
         Assert.assertEquals(expectedRightExpression, arguments[2]);

         return this;
     }

     private final ComparisonEvaluationResult mResult;
     private final ArrayList mInvocations = new ArrayList<>();
 }
 
```

**Returns:**
[IComparisonExpressionEvaluator](../../com.aspose.words/icomparisonexpressionevaluator/) - The field comparison expressions evaluator.
### getCurrentUser() {#getCurrentUser}
```
public UserInformation getCurrentUser()
```


Gets the current user information.

 **Examples:** 

Shows how to set user details, and display them using fields.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a UserInformation object and set it as the data source for fields that display user information.
 UserInformation userInformation = new UserInformation();
 userInformation.setName("John Doe");
 userInformation.setInitials("J. D.");
 userInformation.setAddress("123 Main Street");
 doc.getFieldOptions().setCurrentUser(userInformation);

 // Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
 // the respective properties of the UserInformation object that we have created above.
 Assert.assertEquals(userInformation.getName(), builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals(userInformation.getInitials(), builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals(userInformation.getAddress(), builder.insertField(" USERADDRESS ").getResult());

 // The field options object also has a static default user that fields from all documents can refer to.
 UserInformation.getDefaultUser().setName("Default User");
 UserInformation.getDefaultUser().setInitials("D. U.");
 UserInformation.getDefaultUser().setAddress("One Microsoft Way");
 doc.getFieldOptions().setCurrentUser(UserInformation.getDefaultUser());

 Assert.assertEquals("Default User", builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals("D. U.", builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals("One Microsoft Way", builder.insertField(" USERADDRESS ").getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.CurrentUser.docx");
 
```

**Returns:**
[UserInformation](../../com.aspose.words/userinformation/) - The current user information.
### getCustomTocStyleSeparator() {#getCustomTocStyleSeparator}
```
public String getCustomTocStyleSeparator()
```


Gets custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc/) field.

 **Remarks:** 

By default, custom styles defined by the \\t switch in the [FieldToc](../../com.aspose.words/fieldtoc/) field are separated by a delimiter taken from the current culture. This property overrides that behaviour by specifying a user defined delimiter.

 **Examples:** 

Shows how to insert a TOC, and populate it with entries based on heading styles.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
java.lang.String - Custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc/) field.
### getDefaultDocumentAuthor() {#getDefaultDocumentAuthor}
```
public String getDefaultDocumentAuthor()
```


Gets default document author's name. If author's name is already specified in built-in document properties, this option is not considered.

 **Examples:** 

Shows how to use an AUTHOR field to display a document creator's name.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // AUTHOR fields source their results from the built-in document property called "Author".
 // If we create and save a document in Microsoft Word,
 // it will have our username in that property.
 // However, if we create a document programmatically using Aspose.Words,
 // the "Author" property, by default, will be an empty string.
 Assert.assertEquals("", doc.getBuiltInDocumentProperties().getAuthor());

 // Set a backup author name for AUTHOR fields to use
 // if the "Author" property contains an empty string.
 doc.getFieldOptions().setDefaultDocumentAuthor("Joe Bloggs");

 builder.write("This document was created by ");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);
 field.update();

 Assert.assertEquals(" AUTHOR ", field.getFieldCode());
 Assert.assertEquals("Joe Bloggs", field.getResult());

 // Updating an AUTHOR field that contains a value
 // will apply that value to the "Author" built-in property.
 Assert.assertEquals("Joe Bloggs", doc.getBuiltInDocumentProperties().getAuthor());

 // Changing this property, then updating the AUTHOR field will apply this value to the field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 field.update();

 Assert.assertEquals(" AUTHOR ", field.getFieldCode());
 Assert.assertEquals("John Doe", field.getResult());

 // If we update an AUTHOR field after changing its "Name" property,
 // then the field will display the new name and apply the new name to the built-in property.
 field.setAuthorName("Jane Doe");
 field.update();

 Assert.assertEquals(field.getFieldCode(), " AUTHOR  \"Jane Doe\"");
 Assert.assertEquals(field.getResult(), "Jane Doe");

 // AUTHOR fields do not affect the DefaultDocumentAuthor property.
 Assert.assertEquals("Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());
 Assert.assertEquals("Joe Bloggs", doc.getFieldOptions().getDefaultDocumentAuthor());

 doc.save(getArtifactsDir() + "Field.AUTHOR.docx");
 
```

**Returns:**
java.lang.String - Default document author's name.
### getFieldDatabaseProvider() {#getFieldDatabaseProvider}
```
public IFieldDatabaseProvider getFieldDatabaseProvider()
```


Gets a provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase/) field.

 **Examples:** 

Shows how to extract data from a database and insert it as a field into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This DATABASE field will run a query on a database, and display the result in a table.
 FieldDatabase field = (FieldDatabase) builder.insertField(FieldType.FIELD_DATABASE, true);
 field.setFileName(getDatabaseDir() + "Northwind.accdb");
 field.setConnection("DSN=MS Access Databases");
 field.setQuery("SELECT * FROM [Products]");

 Assert.assertEquals(MessageFormat.format(" DATABASE  \\d {0} \\c \"DSN=MS Access Databases\" \\s \"SELECT * FROM [Products]\"", getDatabaseDir().replace("\\", "\\\\") + "Northwind.accdb"),
         field.getFieldCode());

 // Insert another DATABASE field with a more complex query that sorts all products in descending order by gross sales.
 field = (FieldDatabase) builder.insertField(FieldType.FIELD_DATABASE, true);
 field.setFileName(getMyDir() + "Database\\Northwind.accdb");
 field.setConnection("DSN=MS Access Databases");
 field.setQuery("SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
         "FROM([Products] " +
         "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
         "GROUP BY[Products].ProductName " +
         "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC");

 // These properties have the same function as LIMIT and TOP clauses.
 // Configure them to display only rows 1 to 10 of the query result in the field's table.
 field.setFirstRecord("1");
 field.setLastRecord("10");

 // This property is the index of the format we want to use for our table. The list of table formats is in the "Table AutoFormat..." menu
 // that shows up when we create a DATABASE field in Microsoft Word. Index #10 corresponds to the "Colorful 3" format.
 field.setTableFormat("10");

 // The FormatAttribute property is a string representation of an integer which stores multiple flags.
 // We can patrially apply the format which the TableFormat property points to by setting different flags in this property.
 // The number we use is the sum of a combination of values corresponding to different aspects of the table style.
 // 63 represents 1 (borders) + 2 (shading) + 4 (font) + 8 (color) + 16 (autofit) + 32 (heading rows).
 field.setFormatAttributes("63");
 field.setInsertHeadings(true);
 field.setInsertOnceOnMailMerge(true);

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.DATABASE.docx");
 
```

**Returns:**
[IFieldDatabaseProvider](../../com.aspose.words/ifielddatabaseprovider/) - A provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase/) field.
### getFieldIndexFormat() {#getFieldIndexFormat}
```
public int getFieldIndexFormat()
```


Gets a [getFieldIndexFormat()](../../com.aspose.words/fieldoptions/\#getFieldIndexFormat) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions/\#setFieldIndexFormat-int) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex/) fields in the document.

 **Examples:** 

Shows how to formatting FieldIndex fields.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("A");
 builder.insertBreak(BreakType.LINE_BREAK);
 builder.insertField("XE \"A\"");
 builder.write("B");

 builder.insertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

 doc.getFieldOptions().setFieldIndexFormat(FieldIndexFormat.FANCY);
 doc.updateFields();

 doc.save(getArtifactsDir() + "Field.SetFieldIndexFormat.docx");
 
```

**Returns:**
int - A [getFieldIndexFormat()](../../com.aspose.words/fieldoptions/\#getFieldIndexFormat) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions/\#setFieldIndexFormat-int) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex/) fields in the document. The returned value is one of [FieldIndexFormat](../../com.aspose.words/fieldindexformat/) constants.
### getFieldUpdateCultureProvider() {#getFieldUpdateCultureProvider}
```
public IFieldUpdateCultureProvider getFieldUpdateCultureProvider()
```


Gets a provider that returns a culture object specific for each particular field.

 **Remarks:** 

The provider is requested when the value of [getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions/\#getFieldUpdateCultureSource) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions/\#setFieldUpdateCultureSource-int) is [FieldUpdateCultureSource.FIELD\_CODE](../../com.aspose.words/fieldupdateculturesource/\#FIELD-CODE).

If the provider is present, then the culture object it returns is used for the field update. Otherwise, a system culture is used.

 **Examples:** 

Shows how to specify a culture which parses date/time formatting for each field.

```

 public void defineDateTimeFormatting() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(FieldType.FIELD_TIME, true);

     doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);

     // Set a provider that returns a culture object specific to each field.
     doc.getFieldOptions().setFieldUpdateCultureProvider(new FieldUpdateCultureProvider());

     FieldTime fieldDate = (FieldTime) doc.getRange().getFields().get(0);
     if (fieldDate.getLocaleId() != EditingLanguage.RUSSIAN)
         fieldDate.setLocaleId(EditingLanguage.RUSSIAN);

     doc.save(getArtifactsDir() + "FieldOptions.UpdateDateTimeFormatting.pdf");
 }

 /// 
 /// Provides a CultureInfo object that should be used during the update of a particular field.
 /// 
 private static class FieldUpdateCultureProvider implements IFieldUpdateCultureProvider {
     /// 
     /// Returns a CultureInfo object to be used during the field's update.
     /// 
     public CultureInfo getCulture(String name, Field field) {
         switch (name) {
             case "ru-RU":
                 CultureInfo culture = new CultureInfo(new Locale(name));
                 DateTimeFormatInfo format = culture.getDateTimeFormat();

                 format.setMonthNames(new String[]{"\u043c\u0435\u0441\u044f\u0446 1", "\u043c\u0435\u0441\u044f\u0446 2", "\u043c\u0435\u0441\u044f\u0446 3", "\u043c\u0435\u0441\u044f\u0446 4", "\u043c\u0435\u0441\u044f\u0446 5", "\u043c\u0435\u0441\u044f\u0446 6", "\u043c\u0435\u0441\u044f\u0446 7", "\u043c\u0435\u0441\u044f\u0446 8", "\u043c\u0435\u0441\u044f\u0446 9", "\u043c\u0435\u0441\u044f\u0446 10", "\u043c\u0435\u0441\u044f\u0446 11", "\u043c\u0435\u0441\u044f\u0446 12", ""});
                 format.setMonthGenitiveNames(format.getMonthNames());
                 format.setAbbreviatedMonthNames(new String[]{"\u043c\u0435\u0441 1", "\u043c\u0435\u0441 2", "\u043c\u0435\u0441 3", "\u043c\u0435\u0441 4", "\u043c\u0435\u0441 5", "\u043c\u0435\u0441 6", "\u043c\u0435\u0441 7", "\u043c\u0435\u0441 8", "\u043c\u0435\u0441 9", "\u043c\u0435\u0441 10", "\u043c\u0435\u0441 11", "\u043c\u0435\u0441 12", ""});
                 format.setAbbreviatedMonthGenitiveNames(format.getAbbreviatedMonthNames());

                 format.setDayNames(new String[]{"\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 7", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 1", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 2", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 3", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 4", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 5", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 6"});
                 format.setAbbreviatedDayNames(new String[]{"\u0434\u0435\u043d\u044c 7", "\u0434\u0435\u043d\u044c 1", "\u0434\u0435\u043d\u044c 2", "\u0434\u0435\u043d\u044c 3", "\u0434\u0435\u043d\u044c 4", "\u0434\u0435\u043d\u044c 5", "\u0434\u0435\u043d\u044c 6"});
                 format.setShortestDayNames(new String[]{"\u04347", "\u04341", "\u04342", "\u04343", "\u04344", "\u04345", "\u04346"});

                 format.setAMDesignator("\u0414\u043e \u043f\u043e\u043b\u0443\u0434\u043d\u044f");
                 format.setPMDesignator("\u041f\u043e\u0441\u043b\u0435 \u043f\u043e\u043b\u0443\u0434\u043d\u044f");

                 final String PATTERN = "yyyy MM (MMMM) dd (dddd) hh:mm:ss tt";
                 format.setLongDatePattern(PATTERN);
                 format.setLongTimePattern(PATTERN);
                 format.setShortDatePattern(PATTERN);
                 format.setShortTimePattern(PATTERN);

                 return culture;
             case "en-US":
                 return new CultureInfo(new Locale(name));
             default:
                 return null;
         }
     }
 }
 
```

**Returns:**
[IFieldUpdateCultureProvider](../../com.aspose.words/ifieldupdatecultureprovider/) - A provider that returns a culture object specific for each particular field.
### getFieldUpdateCultureSource() {#getFieldUpdateCultureSource}
```
public int getFieldUpdateCultureSource()
```


Specifies what culture to use to format the field result.

 **Remarks:** 

By default, the culture of the current thread is used.

The setting affects only date/time fields with \\\\@ format switch.

**Returns:**
int - The corresponding  int  value. The returned value is one of [FieldUpdateCultureSource](../../com.aspose.words/fieldupdateculturesource/) constants.
### getFieldUpdatingCallback() {#getFieldUpdatingCallback}
```
public IFieldUpdatingCallback getFieldUpdatingCallback()
```


Gets [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback/) implementation

 **Examples:** 

Shows how to use callback methods during a field update.

```

 public void fieldUpdatingCallbackTest() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");

     FieldUpdatingCallback callback = new FieldUpdatingCallback();
     doc.getFieldOptions().setFieldUpdatingCallback(callback);

     doc.updateFields();

     Assert.assertTrue(callback.getFieldUpdatedCalls().contains("Updating John Doe"));
 }

 /// 
 /// Implement this interface if you want to have your own custom methods called during a field update.
 /// 
 public static class FieldUpdatingCallback implements IFieldUpdatingCallback
 {
     public FieldUpdatingCallback()
     {
         mFieldUpdatedCalls = new ArrayList();
     }

     /// 
     /// A user defined method that is called just before a field is updated.
     /// 
     public void fieldUpdating(Field field) {
         if (field.getType() == FieldType.FIELD_AUTHOR)
         {
             FieldAuthor fieldAuthor = (FieldAuthor) field;
             try {
                 fieldAuthor.setAuthorName("Updating John Doe");
             } catch (Exception e) {
                 e.printStackTrace();
             }
         }
     }

     /// 
     /// A user defined method that is called just after a field is updated.
     /// 
     public void fieldUpdated(Field field)
     {
         getFieldUpdatedCalls().add(field.getResult());
     }

     public ArrayList getFieldUpdatedCalls() { return mFieldUpdatedCalls; };

     private ArrayList mFieldUpdatedCalls;
 }
 
```

**Returns:**
[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback/) - [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback/) implementation
### getFieldUpdatingProgressCallback() {#getFieldUpdatingProgressCallback}
```
public IFieldUpdatingProgressCallback getFieldUpdatingProgressCallback()
```


Gets [IFieldUpdatingProgressCallback](../../com.aspose.words/ifieldupdatingprogresscallback/) implementation.

 **Examples:** 

Shows how to use callback methods during a field update.

```

 public void fieldUpdatingCallbackTest() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");

     FieldUpdatingCallback callback = new FieldUpdatingCallback();
     doc.getFieldOptions().setFieldUpdatingCallback(callback);

     doc.updateFields();

     Assert.assertTrue(callback.getFieldUpdatedCalls().contains("Updating John Doe"));
 }

 /// 
 /// Implement this interface if you want to have your own custom methods called during a field update.
 /// 
 public static class FieldUpdatingCallback implements IFieldUpdatingCallback
 {
     public FieldUpdatingCallback()
     {
         mFieldUpdatedCalls = new ArrayList();
     }

     /// 
     /// A user defined method that is called just before a field is updated.
     /// 
     public void fieldUpdating(Field field) {
         if (field.getType() == FieldType.FIELD_AUTHOR)
         {
             FieldAuthor fieldAuthor = (FieldAuthor) field;
             try {
                 fieldAuthor.setAuthorName("Updating John Doe");
             } catch (Exception e) {
                 e.printStackTrace();
             }
         }
     }

     /// 
     /// A user defined method that is called just after a field is updated.
     /// 
     public void fieldUpdated(Field field)
     {
         getFieldUpdatedCalls().add(field.getResult());
     }

     public ArrayList getFieldUpdatedCalls() { return mFieldUpdatedCalls; };

     private ArrayList mFieldUpdatedCalls;
 }
 
```

**Returns:**
[IFieldUpdatingProgressCallback](../../com.aspose.words/ifieldupdatingprogresscallback/) - [IFieldUpdatingProgressCallback](../../com.aspose.words/ifieldupdatingprogresscallback/) implementation.
### getFileName() {#getFileName}
```
public String getFileName()
```


Gets the file name of the document.

 **Remarks:** 

This property is used by the [FieldFileName](../../com.aspose.words/fieldfilename/) field with higher priority than the [Document.getOriginalFileName()](../../com.aspose.words/document/\#getOriginalFileName) property.

 **Examples:** 

Shows how to use FieldOptions to override the default value for the FILENAME field.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.moveToDocumentEnd();
 builder.writeln();

 // This FILENAME field will display the local system file name of the document we loaded.
 FieldFileName field = (FieldFileName) builder.insertField(FieldType.FIELD_FILE_NAME, true);
 field.update();

 Assert.assertEquals(" FILENAME ", field.getFieldCode());
 Assert.assertEquals("Document.docx", field.getResult());

 builder.writeln();

 // By default, the FILENAME field shows the file's name, but not its full local file system path.
 // We can set a flag to make it show the full file path.
 field = (FieldFileName) builder.insertField(FieldType.FIELD_FILE_NAME, true);
 field.setIncludeFullPath(true);
 field.update();

 Assert.assertEquals(getMyDir() + "Document.docx", field.getResult());

 // We can also set a value for this property to
 // override the value that the FILENAME field displays.
 doc.getFieldOptions().setFileName("FieldOptions.FILENAME.docx");
 field.update();

 Assert.assertEquals(" FILENAME  \\p", field.getFieldCode());
 Assert.assertEquals("FieldOptions.FILENAME.docx", field.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + doc.getFieldOptions().getFileName());
 
```

**Returns:**
java.lang.String - The file name of the document.
### getLegacyNumberFormat() {#getLegacyNumberFormat}
```
public boolean getLegacyNumberFormat()
```


Gets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not.

 **Remarks:** 

When this property is set to  true , template symbol "\#" worked as in .net: Replaces the pound sign with the corresponding digit if one is present; otherwise, no symbols appears in the result string.

When this property is set to  false , template symbol "\#" works as MS Word: This format item specifies the requisite numeric places to display in the result. If the result does not include a digit in that place, MS Word displays a space. For example, \{ = 9 + 6 \\\# $\#\#\# \} displays $ 15.

The default value is  false .

 **Examples:** 

Shows how enable legacy number formatting for fields.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field field = builder.insertField("= 2 + 3 \\# $##");

 Assert.assertEquals("$ 5", field.getResult());

 doc.getFieldOptions().setLegacyNumberFormat(true);
 field.update();

 Assert.assertEquals("$5", field.getResult());
 
```

**Returns:**
boolean - The value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not.
### getPreProcessCulture() {#getPreProcessCulture}
```
public System.Globalization.CultureInfo getPreProcessCulture()
```


Gets the culture to preprocess field values.

 **Remarks:** 

Currently this property only affects value of the [FieldDocProperty](../../com.aspose.words/fielddocproperty/) field.

The default value is  null . When this property is set to  null , the [FieldDocProperty](../../com.aspose.words/fielddocproperty/) field's value is preprocessed with the culture controlled by the [getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions/\#getFieldUpdateCultureSource) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions/\#setFieldUpdateCultureSource-int) property.

 **Examples:** 

Shows how to set the preprocess culture.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the culture according to which some fields will format their displayed values.
 doc.getFieldOptions().setPreProcessCulture(new CultureInfo("de-DE"));

 Field field = builder.insertField(" DOCPROPERTY CreateTime");

 // The DOCPROPERTY field will display its result formatted according to the preprocess culture
 // we have set to German. The field will display the date/time using the "dd.mm.yyyy hh:mm" format.
 Assert.assertTrue(field.getResult().matches("\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}"));

 doc.getFieldOptions().setPreProcessCulture(new CultureInfo(Locale.ROOT));
 field.update();

 // After switching to the invariant culture, the DOCPROPERTY field will use the "mm/dd/yyyy hh:mm" format.
 Assert.assertTrue(field.getResult().matches("\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}"));
 
```

**Returns:**
[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo/) - The culture to preprocess field values.
### getResultFormatter() {#getResultFormatter}
```
public IFieldResultFormatter getResultFormatter()
```


Allows to control how the field result is formatted.

 **Examples:** 

Shows how to automatically apply a custom format to field results as the fields are updated.

```

 public void fieldResultFormatting() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldResultFormatter formatter = new FieldResultFormatter("$%d", "Date: %tb", "Item # %s:");
     doc.getFieldOptions().setResultFormatter(formatter);

     // Our field result formatter applies a custom format to newly created fields of three types of formats.
     // Field result formatters apply new formatting to fields as they are updated,
     // which happens as soon as we create them using this InsertField method overload.
     // 1 -  Numeric:
     builder.insertField(" = 2 + 3 \\# $###");

     Assert.assertEquals("$5", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.NUMERIC));

     // 2 -  Date/time:
     builder.insertField("DATE \\@ \"d MMMM yyyy\"");

     Assert.assertTrue(doc.getRange().getFields().get(1).getResult().startsWith("Date: "));
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.DATE_TIME));

     // 3 -  General:
     builder.insertField("QUOTE \"2\" \\* Ordinal");

     Assert.assertEquals("Item # 2:", doc.getRange().getFields().get(2).getResult());
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.GENERAL));

     formatter.printFormatInvocations();
 }

 /// 
 /// When fields with formatting are updated, this formatter will override their formatting
 /// with a custom format, while tracking every invocation.
 /// 
 private static class FieldResultFormatter implements IFieldResultFormatter {
     public FieldResultFormatter(String numberFormat, String dateFormat, String generalFormat) {
         mNumberFormat = numberFormat;
         mDateFormat = dateFormat;
         mGeneralFormat = generalFormat;
     }

     public String formatNumeric(double value, String format) {
         if (mNumberFormat.isEmpty())
             return null;

         String newValue = String.format(mNumberFormat, (long) value);
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.NUMERIC, value, format, newValue));
         return newValue;
     }

     public String formatDateTime(Date value, String format, int calendarType) {
         if (mDateFormat.isEmpty())
             return null;

         String newValue = String.format(mDateFormat, value);
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.DATE_TIME, MessageFormat.format("{0} ({1})", value, calendarType), format, newValue));
         return newValue;
     }

     public String format(String value, int format) {
         return format((Object) value, format);
     }

     public String format(double value, int format) {
         return format((Object) value, format);
     }

     private String format(Object value, int format) {
         if (mGeneralFormat.isEmpty())
             return null;

         String newValue = String.format(mGeneralFormat, new DecimalFormat("#.###").format(value));
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.GENERAL, value, GeneralFormat.toString(format), newValue));
         return newValue;
     }

     public int countFormatInvocations(int formatInvocationType) {
         if (formatInvocationType == FormatInvocationType.ALL)
             return getFormatInvocations().size();

         return (int) IterableUtils.countMatches(getFormatInvocations(), i -> i.getFormatInvocationType() == formatInvocationType);
     }

     public void printFormatInvocations() {
         for (FormatInvocation f : getFormatInvocations())
             System.out.println(MessageFormat.format("Invocation type:\t{0}\n" +
                     "\tOriginal value:\t\t{1}\n" +
                     "\tOriginal format:\t{2}\n" +
                     "\tNew value:\t\t\t{3}\n", f.getFormatInvocationType(), f.getValue(), f.getOriginalFormat(), f.getNewValue()));
     }

     private final String mNumberFormat;
     private final String mDateFormat;
     private final String mGeneralFormat;

     private ArrayList getFormatInvocations() {
         return mFormatInvocations;
     }

     private final ArrayList mFormatInvocations = new ArrayList<>();

     private static class FormatInvocation {
         public int getFormatInvocationType() {
             return mFormatInvocationType;
         }

         private final int mFormatInvocationType;

         public Object getValue() {
             return mValue;
         }

         private final Object mValue;

         public String getOriginalFormat() {
             return mOriginalFormat;
         }

         private final String mOriginalFormat;

         public String getNewValue() {
             return mNewValue;
         }

         private final String mNewValue;

         public FormatInvocation(int formatInvocationType, Object value, String originalFormat, String newValue) {
             mValue = value;
             mFormatInvocationType = formatInvocationType;
             mOriginalFormat = originalFormat;
             mNewValue = newValue;
         }
     }

     public final class FormatInvocationType {
         private FormatInvocationType() {
         }

         public static final int NUMERIC = 0;
         public static final int DATE_TIME = 1;
         public static final int GENERAL = 2;
         public static final int ALL = 3;

         public static final int length = 4;
     }
 }
 
```

**Returns:**
[IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter/) - The corresponding [IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter/) value.
### getTemplateName() {#getTemplateName}
```
public String getTemplateName()
```


Gets the file name of the template used by the document.

 **Remarks:** 

This property is used by the [FieldTemplate](../../com.aspose.words/fieldtemplate/) field if the [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) property is empty.

If this property is empty, the default template file name  Normal.dotm  is used.

 **Examples:** 

Shows how to use a TEMPLATE field to display the local file system location of a document's template.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can set a template name using by the fields. This property is used when the "doc.AttachedTemplate" is empty.
 // If this property is empty the default template file name "Normal.dotm" is used.
 doc.getFieldOptions().setTemplateName("");

 FieldTemplate field = (FieldTemplate) builder.insertField(FieldType.FIELD_TEMPLATE, false);
 Assert.assertEquals(field.getFieldCode(), " TEMPLATE ");

 builder.writeln();
 field = (FieldTemplate) builder.insertField(FieldType.FIELD_TEMPLATE, false);
 field.setIncludeFullPath(true);

 Assert.assertEquals(field.getFieldCode(), " TEMPLATE  \\p");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TEMPLATE.docx");
 
```

**Returns:**
java.lang.String - The file name of the template used by the document.
### getToaCategories() {#getToaCategories}
```
public ToaCategories getToaCategories()
```


Gets the table of authorities categories.

 **Examples:** 

Shows how to specify a set of categories for TOA fields.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // TOA fields can filter their entries by categories defined in this collection.
 ToaCategories toaCategories = new ToaCategories();
 doc.getFieldOptions().setToaCategories(toaCategories);

 // This collection of categories comes with default values, which we can overwrite with custom values.
 Assert.assertEquals("Cases", toaCategories.get(1));
 Assert.assertEquals("Statutes", toaCategories.get(2));

 toaCategories.set(1, "My Category 1");
 toaCategories.set(2, "My Category 2");

 // We can always access the default values via this collection.
 Assert.assertEquals("Cases", ToaCategories.getDefaultCategories().get(1));
 Assert.assertEquals("Statutes", ToaCategories.getDefaultCategories().get(2));

 // Insert 2 TOA fields. TOA fields create an entry for each TA field in the document.
 // Use the "\c" switch to select the index of a category from our collection.
 //  With this switch, a TOA field will only pick up entries from TA fields that
 // also have a "\c" switch with a matching category index. Each TOA field will also display
 // the name of the category that its "\c" switch points to.
 builder.insertField("TOA \\c 1 \\h", null);
 builder.insertField("TOA \\c 2 \\h", null);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Insert TOA entries across 2 categories. Our first TOA field will receive one entry,
 // from the second TA field whose "\c" switch also points to the first category.
 // The second TOA field will have two entries from the other two TA fields.
 builder.insertField("TA \\c 2 \\l \"entry 1\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 1 \\l \"entry 2\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 2 \\l \"entry 3\"");

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.TOA.Categories.docx");
 
```

**Returns:**
[ToaCategories](../../com.aspose.words/toacategories/) - The table of authorities categories.
### getUseInvariantCultureNumberFormat() {#getUseInvariantCultureNumberFormat}
```
public boolean getUseInvariantCultureNumberFormat()
```


Gets the value indicating that number format is parsed using invariant culture or not

 **Remarks:** 

When this property is set to  true , number format is taken from an invariant culture.

When this property is set to  false , number format is taken from the current thread's culture.

The default value is  false .

 **Examples:** 

Shows how to format numbers according to the invariant culture.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Locale.setDefault(new Locale("de-DE"));
 Field field = builder.insertField(" = 1234567,89 \\# $#,###,###.#");
 field.update();

 // Sometimes, fields may not format their numbers correctly under certain cultures.
 Assert.assertFalse(doc.getFieldOptions().getUseInvariantCultureNumberFormat());
 Assert.assertEquals("$123,456,789.  ", field.getResult());

 // To fix this, we could change the culture for the entire thread.
 // Another way to fix this is to set this flag,
 // which gets all fields to use the invariant culture when formatting numbers.
 // This way allows us to avoid changing the culture for the entire thread.
 doc.getFieldOptions().setUseInvariantCultureNumberFormat(true);
 field.update();
 Assert.assertEquals("$123,456,789.  ", field.getResult());
 
```

**Returns:**
boolean - The value indicating that number format is parsed using invariant culture or not
### getUserPromptRespondent() {#getUserPromptRespondent}
```
public IFieldUserPromptRespondent getUserPromptRespondent()
```


Gets the respondent to user prompts during field update.

 **Remarks:** 

If the value of this property is set to  null , the fields that require user response on prompting (such as [FieldAsk](../../com.aspose.words/fieldask/) or [FieldFillIn](../../com.aspose.words/fieldfillin/)) are not updated.

The default value is  null .

 **Examples:** 

Shows how to create an ASK field, and set its properties.

```

 public void fieldAsk() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Place a field where the response to our ASK field will be placed.
     FieldRef fieldRef = (FieldRef) builder.insertField(FieldType.FIELD_REF, true);
     fieldRef.setBookmarkName("MyAskField");
     builder.writeln();

     Assert.assertEquals(" REF  MyAskField", fieldRef.getFieldCode());

     // Insert the ASK field and edit its properties to reference our REF field by bookmark name.
     FieldAsk fieldAsk = (FieldAsk) builder.insertField(FieldType.FIELD_ASK, true);
     fieldAsk.setBookmarkName("MyAskField");
     fieldAsk.setPromptText("Please provide a response for this ASK field");
     fieldAsk.setDefaultResponse("Response from within the field.");
     fieldAsk.setPromptOnceOnMailMerge(true);
     builder.writeln();

     Assert.assertEquals(
             " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
             fieldAsk.getFieldCode());

     // ASK fields apply the default response to their respective REF fields during a mail merge.
     DataTable table = new DataTable("My Table");
     table.getColumns().add("Column 1");
     table.getRows().add("Row 1");
     table.getRows().add("Row 2");

     FieldMergeField fieldMergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     fieldMergeField.setFieldName("Column 1");

     // We can modify or override the default response in our ASK fields with a custom prompt responder,
     // which will occur during a mail merge.
     doc.getFieldOptions().setUserPromptRespondent(new MyPromptRespondent());
     doc.getMailMerge().execute(table);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.ASK.docx");
 }

 /// 
 /// Prepends text to the default response of an ASK field during a mail merge.
 /// 
 private static class MyPromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response from MyPromptRespondent. " + defaultResponse;
     }
 }
 
```

**Returns:**
[IFieldUserPromptRespondent](../../com.aspose.words/ifielduserpromptrespondent/) - The respondent to user prompts during field update.
### isBidiTextSupportedOnUpdate() {#isBidiTextSupportedOnUpdate}
```
public boolean isBidiTextSupportedOnUpdate()
```


Gets the value indicating whether bidirectional text is fully supported during field update or not.

 **Remarks:** 

When this property is set to  true , additional steps are performed to produce Right-To-Left language (i.e. Arabic or Hebrew) compatible field result during its update.

When this property is set to  false  and Right-To-Left language is used, correctness of field result after its update is not guaranteed.

The default value is  false .

 **Examples:** 

Shows how to use FieldOptions to ensure that field updating fully supports bi-directional text.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Ensure that any field operation involving right-to-left text is performs as expected.
 doc.getFieldOptions().isBidiTextSupportedOnUpdate(true);

 // Use a document builder to insert a field that contains the right-to-left text.
 FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"\u05e2\u05b6\u05e9\u05b0\u05c2\u05e8\u05b4\u05d9\u05dd", "\u05e9\u05b0\u05c1\u05dc\u05d5\u05b9\u05e9\u05b4\u05c1\u05d9\u05dd", "\u05d0\u05b7\u05e8\u05b0\u05d1\u05b8\u05bc\u05e2\u05b4\u05d9\u05dd", "\u05d7\u05b2\u05de\u05b4\u05e9\u05b4\u05bc\u05c1\u05d9\u05dd", "\u05e9\u05b4\u05c1\u05e9\u05b4\u05bc\u05c1\u05d9\u05dd"}, 0);
 comboBox.setCalculateOnExit(true);

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.Bidi.docx");
 
```

**Returns:**
boolean - The value indicating whether bidirectional text is fully supported during field update or not.
### isBidiTextSupportedOnUpdate(boolean value) {#isBidiTextSupportedOnUpdate-boolean}
```
public void isBidiTextSupportedOnUpdate(boolean value)
```


Sets the value indicating whether bidirectional text is fully supported during field update or not.

 **Remarks:** 

When this property is set to  true , additional steps are performed to produce Right-To-Left language (i.e. Arabic or Hebrew) compatible field result during its update.

When this property is set to  false  and Right-To-Left language is used, correctness of field result after its update is not guaranteed.

The default value is  false .

 **Examples:** 

Shows how to use FieldOptions to ensure that field updating fully supports bi-directional text.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Ensure that any field operation involving right-to-left text is performs as expected.
 doc.getFieldOptions().isBidiTextSupportedOnUpdate(true);

 // Use a document builder to insert a field that contains the right-to-left text.
 FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"\u05e2\u05b6\u05e9\u05b0\u05c2\u05e8\u05b4\u05d9\u05dd", "\u05e9\u05b0\u05c1\u05dc\u05d5\u05b9\u05e9\u05b4\u05c1\u05d9\u05dd", "\u05d0\u05b7\u05e8\u05b0\u05d1\u05b8\u05bc\u05e2\u05b4\u05d9\u05dd", "\u05d7\u05b2\u05de\u05b4\u05e9\u05b4\u05bc\u05c1\u05d9\u05dd", "\u05e9\u05b4\u05c1\u05e9\u05b4\u05bc\u05c1\u05d9\u05dd"}, 0);
 comboBox.setCalculateOnExit(true);

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.Bidi.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The value indicating whether bidirectional text is fully supported during field update or not. |

### setBarcodeGenerator(IBarcodeGenerator value) {#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator}
```
public void setBarcodeGenerator(IBarcodeGenerator value)
```


Gets or set custom barcode generator.

 **Remarks:** 

Custom barcode generator should implement public interface [IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator/).

 **Examples:** 

Shows how to use a barcode generator.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // We can use a custom IBarcodeGenerator implementation to generate barcodes,
 // and then insert them into the document as images.
 doc.getFieldOptions().setBarcodeGenerator(new CustomBarcodeGenerator());

 // Below are four examples of different barcode types that we can create using our generator.
 // For each barcode, we specify a new set of barcode parameters, and then generate the image.
 // Afterwards, we can insert the image into the document, or save it to the local file system.
 // 1 -  QR code:
 BarcodeParameters barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("QR");
     barcodeParameters.setBarcodeValue("ABC123");
     barcodeParameters.setBackgroundColor("0xF8BD69");
     barcodeParameters.setForegroundColor("0xB5413B");
     barcodeParameters.setErrorCorrectionLevel("3");
     barcodeParameters.setScalingFactor("250");
     barcodeParameters.setSymbolHeight("1000");
     barcodeParameters.setSymbolRotation("0");
 }

 BufferedImage img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.QR.jpg"));

 builder.insertImage(img);

 // 2 -  EAN13 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("EAN13");
     barcodeParameters.setBarcodeValue("501234567890");
     barcodeParameters.setDisplayText(true);
     barcodeParameters.setPosCodeStyle("CASE");
     barcodeParameters.setFixCheckDigit(true);
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.EAN13.jpg"));
 builder.insertImage(img);

 // 3 -  CODE39 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("CODE39");
     barcodeParameters.setBarcodeValue("12345ABCDE");
     barcodeParameters.setAddStartStopChar(true);
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.CODE39.jpg"));
 builder.insertImage(img);

 // 4 -  ITF14 barcode:
 barcodeParameters = new BarcodeParameters();
 {
     barcodeParameters.setBarcodeType("ITF14");
     barcodeParameters.setBarcodeValue("09312345678907");
     barcodeParameters.setCaseCodeStyle("STD");
 }

 img = doc.getFieldOptions().getBarcodeGenerator().getBarcodeImage(barcodeParameters);
 ImageIO.write(img, "jpg", new File(getArtifactsDir() + "FieldOptions.BarcodeGenerator.ITF14.jpg"));
 builder.insertImage(img);

 doc.save(getArtifactsDir() + "FieldOptions.BarcodeGenerator.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator/) | Or set custom barcode generator. |

### setBibliographyStylesProvider(IBibliographyStylesProvider value) {#setBibliographyStylesProvider-com.aspose.words.IBibliographyStylesProvider}
```
public void setBibliographyStylesProvider(IBibliographyStylesProvider value)
```


Sets a provider that returns a bibliography style for the [FieldBibliography](../../com.aspose.words/fieldbibliography/) and [FieldCitation](../../com.aspose.words/fieldcitation/) fields.

 **Examples:** 

Shows how to override built-in styles or provide custom one.

```

 public void changeBibliographyStyles() throws Exception
 {
     Document doc = new Document(getMyDir() + "Bibliography.docx");

     // If the document already has a style you can change it with the following code:
     // doc.Bibliography.BibliographyStyle = "Bibliography custom style.xsl";

     doc.getFieldOptions().setBibliographyStylesProvider(new BibliographyStylesProvider());
     doc.updateFields();

     doc.save(getArtifactsDir() + "Field.ChangeBibliographyStyles.docx");
 }

 public static class BibliographyStylesProvider implements IBibliographyStylesProvider
 {
     public FileInputStream getStyle(String styleFileName) throws Exception
     {
         return new FileInputStream(getMyDir() + "Bibliography custom style.xsl");
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IBibliographyStylesProvider](../../com.aspose.words/ibibliographystylesprovider/) | A provider that returns a bibliography style for the [FieldBibliography](../../com.aspose.words/fieldbibliography/) and [FieldCitation](../../com.aspose.words/fieldcitation/) fields. |

### setBuiltInTemplatesPaths(String[] value) {#setBuiltInTemplatesPaths-java.lang.String}
```
public void setBuiltInTemplatesPaths(String[] value)
```


Sets paths of MS Word built-in templates.

 **Remarks:** 

This property is used by the [FieldAutoText](../../com.aspose.words/fieldautotext/) and [FieldGlossary](../../com.aspose.words/fieldglossary/) fields, if referenced auto text entry is not found in the [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) template.

By default MS Word stores built-in templates in c:\\Users\\\\AppData\\Roaming\\Microsoft\\Document Building Blocks\\1033\\16\\Built-In Building Blocks.dotx and C:\\Users\\\\AppData\\Roaming\\Microsoft\\Templates\\Normal.dotm files.

 **Examples:** 

Shows how to display a building block with AUTOTEXT and GLOSSARY fields.

```

 Document doc = new Document();

 // Create a glossary document and add an AutoText building block to it.
 doc.setGlossaryDocument(new GlossaryDocument());
 BuildingBlock buildingBlock = new BuildingBlock(doc.getGlossaryDocument());
 buildingBlock.setName("MyBlock");
 buildingBlock.setGallery(BuildingBlockGallery.AUTO_TEXT);
 buildingBlock.setCategory("General");
 buildingBlock.setDescription("MyBlock description");
 buildingBlock.setBehavior(BuildingBlockBehavior.PARAGRAPH);
 doc.getGlossaryDocument().appendChild(buildingBlock);

 // Create a source and add it as text to our building block.
 Document buildingBlockSource = new Document();
 DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
 buildingBlockSourceBuilder.writeln("Hello World!");

 Node buildingBlockContent = doc.getGlossaryDocument().importNode(buildingBlockSource.getFirstSection(), true);
 buildingBlock.appendChild(buildingBlockContent);

 // Set a file which contains parts that our document, or its attached template may not contain.
 doc.getFieldOptions().setBuiltInTemplatesPaths(new String[]{getMyDir() + "Busniess brochure.dotx"});

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways to use fields to display the contents of our building block.
 // 1 -  Using an AUTOTEXT field:
 FieldAutoText fieldAutoText = (FieldAutoText) builder.insertField(FieldType.FIELD_AUTO_TEXT, true);
 fieldAutoText.setEntryName("MyBlock");

 Assert.assertEquals(" AUTOTEXT  MyBlock", fieldAutoText.getFieldCode());

 // 2 -  Using a GLOSSARY field:
 FieldGlossary fieldGlossary = (FieldGlossary) builder.insertField(FieldType.FIELD_GLOSSARY, true);
 fieldGlossary.setEntryName("MyBlock");

 Assert.assertEquals(fieldGlossary.getFieldCode(), " GLOSSARY  MyBlock");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.AUTOTEXT.GLOSSARY.dotx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String[] | Paths of MS Word built-in templates. |

### setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value) {#setComparisonExpressionEvaluator-com.aspose.words.IComparisonExpressionEvaluator}
```
public void setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value)
```


Sets the field comparison expressions evaluator.

 **Examples:** 

Shows how to implement custom evaluation for the IF and COMPARE fields.

```

 public void conditionEvaluationExtensionPoint(String fieldCode, byte comparisonResult, String comparisonError,
                                               String expectedResult) throws Exception {
     final String LEFT = "\"left expression\"";
     final String _OPERATOR = "<>";
     final String RIGHT = "\"right expression\"";

     DocumentBuilder builder = new DocumentBuilder();

     // Field codes that we use in this example:
     // 1.   " IF %s %s %s \"true argument\" \"false argument\" ".
     // 2.   " COMPARE %s %s %s ".
     Field field = builder.insertField(String.format(fieldCode, LEFT, _OPERATOR, RIGHT), null);

     // If the "comparisonResult" is undefined, we create "ComparisonEvaluationResult" with string, instead of bool.
     ComparisonEvaluationResult result = comparisonResult != -1
             ? new ComparisonEvaluationResult(comparisonResult == 1)
             : comparisonError != null ? new ComparisonEvaluationResult(comparisonError) : null;

     ComparisonExpressionEvaluator evaluator = new ComparisonExpressionEvaluator(result);
     builder.getDocument().getFieldOptions().setComparisonExpressionEvaluator(evaluator);

     builder.getDocument().updateFields();

     Assert.assertEquals(expectedResult, field.getResult());
     evaluator.assertInvocationsCount(1).assertInvocationArguments(0, LEFT, _OPERATOR, RIGHT);
 }

 public static Object[][] conditionEvaluationExtensionPointDataProvider() {
     return new Object[][]
             {
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) 1, null, "true argument"},
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) 0, null, "false argument"},
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) -1, "Custom Error", "Custom Error"},
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) -1, null, "true argument"},
                     {" COMPARE %s %s %s ", (byte) 1, null, "1"},
                     {" COMPARE %s %s %s ", (byte) 0, null, "0"},
                     {" COMPARE %s %s %s ", (byte) -1, "Custom Error", "Custom Error"},
                     {" COMPARE %s %s %s ", (byte) -1, null, "1"},
             };
 }

 /// 
 /// Comparison expressions evaluation for the FieldIf and FieldCompare.
 /// 
 private static class ComparisonExpressionEvaluator implements IComparisonExpressionEvaluator {
     public ComparisonExpressionEvaluator(ComparisonEvaluationResult result) {
         mResult = result;
     }

     public ComparisonEvaluationResult evaluate(Field field, ComparisonExpression expression) {
         mInvocations.add(new String[]
                 {
                         expression.getLeftExpression(),
                         expression.getComparisonOperator(),
                         expression.getRightExpression()
                 });

         return mResult;
     }

     public ComparisonExpressionEvaluator assertInvocationsCount(int expected) {
         Assert.assertEquals(expected, mInvocations.size());
         return this;
     }

     public ComparisonExpressionEvaluator assertInvocationArguments(
             int invocationIndex,
             String expectedLeftExpression,
             String expectedComparisonOperator,
             String expectedRightExpression) {
         String[] arguments = mInvocations.get(invocationIndex);

         Assert.assertEquals(expectedLeftExpression, arguments[0]);
         Assert.assertEquals(expectedComparisonOperator, arguments[1]);
         Assert.assertEquals(expectedRightExpression, arguments[2]);

         return this;
     }

     private final ComparisonEvaluationResult mResult;
     private final ArrayList mInvocations = new ArrayList<>();
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IComparisonExpressionEvaluator](../../com.aspose.words/icomparisonexpressionevaluator/) | The field comparison expressions evaluator. |

### setCurrentUser(UserInformation value) {#setCurrentUser-com.aspose.words.UserInformation}
```
public void setCurrentUser(UserInformation value)
```


Sets the current user information.

 **Examples:** 

Shows how to set user details, and display them using fields.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a UserInformation object and set it as the data source for fields that display user information.
 UserInformation userInformation = new UserInformation();
 userInformation.setName("John Doe");
 userInformation.setInitials("J. D.");
 userInformation.setAddress("123 Main Street");
 doc.getFieldOptions().setCurrentUser(userInformation);

 // Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
 // the respective properties of the UserInformation object that we have created above.
 Assert.assertEquals(userInformation.getName(), builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals(userInformation.getInitials(), builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals(userInformation.getAddress(), builder.insertField(" USERADDRESS ").getResult());

 // The field options object also has a static default user that fields from all documents can refer to.
 UserInformation.getDefaultUser().setName("Default User");
 UserInformation.getDefaultUser().setInitials("D. U.");
 UserInformation.getDefaultUser().setAddress("One Microsoft Way");
 doc.getFieldOptions().setCurrentUser(UserInformation.getDefaultUser());

 Assert.assertEquals("Default User", builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals("D. U.", builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals("One Microsoft Way", builder.insertField(" USERADDRESS ").getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.CurrentUser.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [UserInformation](../../com.aspose.words/userinformation/) | The current user information. |

### setCustomTocStyleSeparator(String value) {#setCustomTocStyleSeparator-java.lang.String}
```
public void setCustomTocStyleSeparator(String value)
```


Sets custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc/) field.

 **Remarks:** 

By default, custom styles defined by the \\t switch in the [FieldToc](../../com.aspose.words/fieldtoc/) field are separated by a delimiter taken from the current culture. This property overrides that behaviour by specifying a user defined delimiter.

 **Examples:** 

Shows how to insert a TOC, and populate it with entries based on heading styles.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc/) field. |

### setDefaultDocumentAuthor(String value) {#setDefaultDocumentAuthor-java.lang.String}
```
public void setDefaultDocumentAuthor(String value)
```


Sets default document author's name. If author's name is already specified in built-in document properties, this option is not considered.

 **Examples:** 

Shows how to use an AUTHOR field to display a document creator's name.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // AUTHOR fields source their results from the built-in document property called "Author".
 // If we create and save a document in Microsoft Word,
 // it will have our username in that property.
 // However, if we create a document programmatically using Aspose.Words,
 // the "Author" property, by default, will be an empty string.
 Assert.assertEquals("", doc.getBuiltInDocumentProperties().getAuthor());

 // Set a backup author name for AUTHOR fields to use
 // if the "Author" property contains an empty string.
 doc.getFieldOptions().setDefaultDocumentAuthor("Joe Bloggs");

 builder.write("This document was created by ");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);
 field.update();

 Assert.assertEquals(" AUTHOR ", field.getFieldCode());
 Assert.assertEquals("Joe Bloggs", field.getResult());

 // Updating an AUTHOR field that contains a value
 // will apply that value to the "Author" built-in property.
 Assert.assertEquals("Joe Bloggs", doc.getBuiltInDocumentProperties().getAuthor());

 // Changing this property, then updating the AUTHOR field will apply this value to the field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 field.update();

 Assert.assertEquals(" AUTHOR ", field.getFieldCode());
 Assert.assertEquals("John Doe", field.getResult());

 // If we update an AUTHOR field after changing its "Name" property,
 // then the field will display the new name and apply the new name to the built-in property.
 field.setAuthorName("Jane Doe");
 field.update();

 Assert.assertEquals(field.getFieldCode(), " AUTHOR  \"Jane Doe\"");
 Assert.assertEquals(field.getResult(), "Jane Doe");

 // AUTHOR fields do not affect the DefaultDocumentAuthor property.
 Assert.assertEquals("Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());
 Assert.assertEquals("Joe Bloggs", doc.getFieldOptions().getDefaultDocumentAuthor());

 doc.save(getArtifactsDir() + "Field.AUTHOR.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Default document author's name. |

### setFieldDatabaseProvider(IFieldDatabaseProvider value) {#setFieldDatabaseProvider-com.aspose.words.IFieldDatabaseProvider}
```
public void setFieldDatabaseProvider(IFieldDatabaseProvider value)
```


Sets a provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase/) field.

 **Examples:** 

Shows how to extract data from a database and insert it as a field into a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This DATABASE field will run a query on a database, and display the result in a table.
 FieldDatabase field = (FieldDatabase) builder.insertField(FieldType.FIELD_DATABASE, true);
 field.setFileName(getDatabaseDir() + "Northwind.accdb");
 field.setConnection("DSN=MS Access Databases");
 field.setQuery("SELECT * FROM [Products]");

 Assert.assertEquals(MessageFormat.format(" DATABASE  \\d {0} \\c \"DSN=MS Access Databases\" \\s \"SELECT * FROM [Products]\"", getDatabaseDir().replace("\\", "\\\\") + "Northwind.accdb"),
         field.getFieldCode());

 // Insert another DATABASE field with a more complex query that sorts all products in descending order by gross sales.
 field = (FieldDatabase) builder.insertField(FieldType.FIELD_DATABASE, true);
 field.setFileName(getMyDir() + "Database\\Northwind.accdb");
 field.setConnection("DSN=MS Access Databases");
 field.setQuery("SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
         "FROM([Products] " +
         "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
         "GROUP BY[Products].ProductName " +
         "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC");

 // These properties have the same function as LIMIT and TOP clauses.
 // Configure them to display only rows 1 to 10 of the query result in the field's table.
 field.setFirstRecord("1");
 field.setLastRecord("10");

 // This property is the index of the format we want to use for our table. The list of table formats is in the "Table AutoFormat..." menu
 // that shows up when we create a DATABASE field in Microsoft Word. Index #10 corresponds to the "Colorful 3" format.
 field.setTableFormat("10");

 // The FormatAttribute property is a string representation of an integer which stores multiple flags.
 // We can patrially apply the format which the TableFormat property points to by setting different flags in this property.
 // The number we use is the sum of a combination of values corresponding to different aspects of the table style.
 // 63 represents 1 (borders) + 2 (shading) + 4 (font) + 8 (color) + 16 (autofit) + 32 (heading rows).
 field.setFormatAttributes("63");
 field.setInsertHeadings(true);
 field.setInsertOnceOnMailMerge(true);

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.DATABASE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldDatabaseProvider](../../com.aspose.words/ifielddatabaseprovider/) | A provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase/) field. |

### setFieldIndexFormat(int value) {#setFieldIndexFormat-int}
```
public void setFieldIndexFormat(int value)
```


Sets a [getFieldIndexFormat()](../../com.aspose.words/fieldoptions/\#getFieldIndexFormat) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions/\#setFieldIndexFormat-int) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex/) fields in the document.

 **Examples:** 

Shows how to formatting FieldIndex fields.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("A");
 builder.insertBreak(BreakType.LINE_BREAK);
 builder.insertField("XE \"A\"");
 builder.write("B");

 builder.insertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

 doc.getFieldOptions().setFieldIndexFormat(FieldIndexFormat.FANCY);
 doc.updateFields();

 doc.save(getArtifactsDir() + "Field.SetFieldIndexFormat.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A [getFieldIndexFormat()](../../com.aspose.words/fieldoptions/\#getFieldIndexFormat) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions/\#setFieldIndexFormat-int) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex/) fields in the document. The value must be one of [FieldIndexFormat](../../com.aspose.words/fieldindexformat/) constants. |

### setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value) {#setFieldUpdateCultureProvider-com.aspose.words.IFieldUpdateCultureProvider}
```
public void setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value)
```


Sets a provider that returns a culture object specific for each particular field.

 **Remarks:** 

The provider is requested when the value of [getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions/\#getFieldUpdateCultureSource) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions/\#setFieldUpdateCultureSource-int) is [FieldUpdateCultureSource.FIELD\_CODE](../../com.aspose.words/fieldupdateculturesource/\#FIELD-CODE).

If the provider is present, then the culture object it returns is used for the field update. Otherwise, a system culture is used.

 **Examples:** 

Shows how to specify a culture which parses date/time formatting for each field.

```

 public void defineDateTimeFormatting() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(FieldType.FIELD_TIME, true);

     doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);

     // Set a provider that returns a culture object specific to each field.
     doc.getFieldOptions().setFieldUpdateCultureProvider(new FieldUpdateCultureProvider());

     FieldTime fieldDate = (FieldTime) doc.getRange().getFields().get(0);
     if (fieldDate.getLocaleId() != EditingLanguage.RUSSIAN)
         fieldDate.setLocaleId(EditingLanguage.RUSSIAN);

     doc.save(getArtifactsDir() + "FieldOptions.UpdateDateTimeFormatting.pdf");
 }

 /// 
 /// Provides a CultureInfo object that should be used during the update of a particular field.
 /// 
 private static class FieldUpdateCultureProvider implements IFieldUpdateCultureProvider {
     /// 
     /// Returns a CultureInfo object to be used during the field's update.
     /// 
     public CultureInfo getCulture(String name, Field field) {
         switch (name) {
             case "ru-RU":
                 CultureInfo culture = new CultureInfo(new Locale(name));
                 DateTimeFormatInfo format = culture.getDateTimeFormat();

                 format.setMonthNames(new String[]{"\u043c\u0435\u0441\u044f\u0446 1", "\u043c\u0435\u0441\u044f\u0446 2", "\u043c\u0435\u0441\u044f\u0446 3", "\u043c\u0435\u0441\u044f\u0446 4", "\u043c\u0435\u0441\u044f\u0446 5", "\u043c\u0435\u0441\u044f\u0446 6", "\u043c\u0435\u0441\u044f\u0446 7", "\u043c\u0435\u0441\u044f\u0446 8", "\u043c\u0435\u0441\u044f\u0446 9", "\u043c\u0435\u0441\u044f\u0446 10", "\u043c\u0435\u0441\u044f\u0446 11", "\u043c\u0435\u0441\u044f\u0446 12", ""});
                 format.setMonthGenitiveNames(format.getMonthNames());
                 format.setAbbreviatedMonthNames(new String[]{"\u043c\u0435\u0441 1", "\u043c\u0435\u0441 2", "\u043c\u0435\u0441 3", "\u043c\u0435\u0441 4", "\u043c\u0435\u0441 5", "\u043c\u0435\u0441 6", "\u043c\u0435\u0441 7", "\u043c\u0435\u0441 8", "\u043c\u0435\u0441 9", "\u043c\u0435\u0441 10", "\u043c\u0435\u0441 11", "\u043c\u0435\u0441 12", ""});
                 format.setAbbreviatedMonthGenitiveNames(format.getAbbreviatedMonthNames());

                 format.setDayNames(new String[]{"\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 7", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 1", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 2", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 3", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 4", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 5", "\u0434\u0435\u043d\u044c \u043d\u0435\u0434\u0435\u043b\u0438 6"});
                 format.setAbbreviatedDayNames(new String[]{"\u0434\u0435\u043d\u044c 7", "\u0434\u0435\u043d\u044c 1", "\u0434\u0435\u043d\u044c 2", "\u0434\u0435\u043d\u044c 3", "\u0434\u0435\u043d\u044c 4", "\u0434\u0435\u043d\u044c 5", "\u0434\u0435\u043d\u044c 6"});
                 format.setShortestDayNames(new String[]{"\u04347", "\u04341", "\u04342", "\u04343", "\u04344", "\u04345", "\u04346"});

                 format.setAMDesignator("\u0414\u043e \u043f\u043e\u043b\u0443\u0434\u043d\u044f");
                 format.setPMDesignator("\u041f\u043e\u0441\u043b\u0435 \u043f\u043e\u043b\u0443\u0434\u043d\u044f");

                 final String PATTERN = "yyyy MM (MMMM) dd (dddd) hh:mm:ss tt";
                 format.setLongDatePattern(PATTERN);
                 format.setLongTimePattern(PATTERN);
                 format.setShortDatePattern(PATTERN);
                 format.setShortTimePattern(PATTERN);

                 return culture;
             case "en-US":
                 return new CultureInfo(new Locale(name));
             default:
                 return null;
         }
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldUpdateCultureProvider](../../com.aspose.words/ifieldupdatecultureprovider/) | A provider that returns a culture object specific for each particular field. |

### setFieldUpdateCultureSource(int value) {#setFieldUpdateCultureSource-int}
```
public void setFieldUpdateCultureSource(int value)
```


Specifies what culture to use to format the field result.

 **Remarks:** 

By default, the culture of the current thread is used.

The setting affects only date/time fields with \\\\@ format switch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FieldUpdateCultureSource](../../com.aspose.words/fieldupdateculturesource/) constants. |

### setFieldUpdatingCallback(IFieldUpdatingCallback value) {#setFieldUpdatingCallback-com.aspose.words.IFieldUpdatingCallback}
```
public void setFieldUpdatingCallback(IFieldUpdatingCallback value)
```


Sets [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback/) implementation

 **Examples:** 

Shows how to use callback methods during a field update.

```

 public void fieldUpdatingCallbackTest() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");

     FieldUpdatingCallback callback = new FieldUpdatingCallback();
     doc.getFieldOptions().setFieldUpdatingCallback(callback);

     doc.updateFields();

     Assert.assertTrue(callback.getFieldUpdatedCalls().contains("Updating John Doe"));
 }

 /// 
 /// Implement this interface if you want to have your own custom methods called during a field update.
 /// 
 public static class FieldUpdatingCallback implements IFieldUpdatingCallback
 {
     public FieldUpdatingCallback()
     {
         mFieldUpdatedCalls = new ArrayList();
     }

     /// 
     /// A user defined method that is called just before a field is updated.
     /// 
     public void fieldUpdating(Field field) {
         if (field.getType() == FieldType.FIELD_AUTHOR)
         {
             FieldAuthor fieldAuthor = (FieldAuthor) field;
             try {
                 fieldAuthor.setAuthorName("Updating John Doe");
             } catch (Exception e) {
                 e.printStackTrace();
             }
         }
     }

     /// 
     /// A user defined method that is called just after a field is updated.
     /// 
     public void fieldUpdated(Field field)
     {
         getFieldUpdatedCalls().add(field.getResult());
     }

     public ArrayList getFieldUpdatedCalls() { return mFieldUpdatedCalls; };

     private ArrayList mFieldUpdatedCalls;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback/) | [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback/) implementation |

### setFieldUpdatingProgressCallback(IFieldUpdatingProgressCallback value) {#setFieldUpdatingProgressCallback-com.aspose.words.IFieldUpdatingProgressCallback}
```
public void setFieldUpdatingProgressCallback(IFieldUpdatingProgressCallback value)
```


Sets [IFieldUpdatingProgressCallback](../../com.aspose.words/ifieldupdatingprogresscallback/) implementation.

 **Examples:** 

Shows how to use callback methods during a field update.

```

 public void fieldUpdatingCallbackTest() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");

     FieldUpdatingCallback callback = new FieldUpdatingCallback();
     doc.getFieldOptions().setFieldUpdatingCallback(callback);

     doc.updateFields();

     Assert.assertTrue(callback.getFieldUpdatedCalls().contains("Updating John Doe"));
 }

 /// 
 /// Implement this interface if you want to have your own custom methods called during a field update.
 /// 
 public static class FieldUpdatingCallback implements IFieldUpdatingCallback
 {
     public FieldUpdatingCallback()
     {
         mFieldUpdatedCalls = new ArrayList();
     }

     /// 
     /// A user defined method that is called just before a field is updated.
     /// 
     public void fieldUpdating(Field field) {
         if (field.getType() == FieldType.FIELD_AUTHOR)
         {
             FieldAuthor fieldAuthor = (FieldAuthor) field;
             try {
                 fieldAuthor.setAuthorName("Updating John Doe");
             } catch (Exception e) {
                 e.printStackTrace();
             }
         }
     }

     /// 
     /// A user defined method that is called just after a field is updated.
     /// 
     public void fieldUpdated(Field field)
     {
         getFieldUpdatedCalls().add(field.getResult());
     }

     public ArrayList getFieldUpdatedCalls() { return mFieldUpdatedCalls; };

     private ArrayList mFieldUpdatedCalls;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldUpdatingProgressCallback](../../com.aspose.words/ifieldupdatingprogresscallback/) | [IFieldUpdatingProgressCallback](../../com.aspose.words/ifieldupdatingprogresscallback/) implementation. |

### setFileName(String value) {#setFileName-java.lang.String}
```
public void setFileName(String value)
```


Sets the file name of the document.

 **Remarks:** 

This property is used by the [FieldFileName](../../com.aspose.words/fieldfilename/) field with higher priority than the [Document.getOriginalFileName()](../../com.aspose.words/document/\#getOriginalFileName) property.

 **Examples:** 

Shows how to use FieldOptions to override the default value for the FILENAME field.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.moveToDocumentEnd();
 builder.writeln();

 // This FILENAME field will display the local system file name of the document we loaded.
 FieldFileName field = (FieldFileName) builder.insertField(FieldType.FIELD_FILE_NAME, true);
 field.update();

 Assert.assertEquals(" FILENAME ", field.getFieldCode());
 Assert.assertEquals("Document.docx", field.getResult());

 builder.writeln();

 // By default, the FILENAME field shows the file's name, but not its full local file system path.
 // We can set a flag to make it show the full file path.
 field = (FieldFileName) builder.insertField(FieldType.FIELD_FILE_NAME, true);
 field.setIncludeFullPath(true);
 field.update();

 Assert.assertEquals(getMyDir() + "Document.docx", field.getResult());

 // We can also set a value for this property to
 // override the value that the FILENAME field displays.
 doc.getFieldOptions().setFileName("FieldOptions.FILENAME.docx");
 field.update();

 Assert.assertEquals(" FILENAME  \\p", field.getFieldCode());
 Assert.assertEquals("FieldOptions.FILENAME.docx", field.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + doc.getFieldOptions().getFileName());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name of the document. |

### setLegacyNumberFormat(boolean value) {#setLegacyNumberFormat-boolean}
```
public void setLegacyNumberFormat(boolean value)
```


Sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not.

 **Remarks:** 

When this property is set to  true , template symbol "\#" worked as in .net: Replaces the pound sign with the corresponding digit if one is present; otherwise, no symbols appears in the result string.

When this property is set to  false , template symbol "\#" works as MS Word: This format item specifies the requisite numeric places to display in the result. If the result does not include a digit in that place, MS Word displays a space. For example, \{ = 9 + 6 \\\# $\#\#\# \} displays $ 15.

The default value is  false .

 **Examples:** 

Shows how enable legacy number formatting for fields.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field field = builder.insertField("= 2 + 3 \\# $##");

 Assert.assertEquals("$ 5", field.getResult());

 doc.getFieldOptions().setLegacyNumberFormat(true);
 field.update();

 Assert.assertEquals("$5", field.getResult());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not. |

### setPreProcessCulture(System.Globalization.CultureInfo value) {#setPreProcessCulture-com.aspose.words.net.System.Globalization.CultureInfo}
```
public void setPreProcessCulture(System.Globalization.CultureInfo value)
```


Sets the culture to preprocess field values.

 **Remarks:** 

Currently this property only affects value of the [FieldDocProperty](../../com.aspose.words/fielddocproperty/) field.

The default value is  null . When this property is set to  null , the [FieldDocProperty](../../com.aspose.words/fielddocproperty/) field's value is preprocessed with the culture controlled by the [getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions/\#getFieldUpdateCultureSource) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions/\#setFieldUpdateCultureSource-int) property.

 **Examples:** 

Shows how to set the preprocess culture.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set the culture according to which some fields will format their displayed values.
 doc.getFieldOptions().setPreProcessCulture(new CultureInfo("de-DE"));

 Field field = builder.insertField(" DOCPROPERTY CreateTime");

 // The DOCPROPERTY field will display its result formatted according to the preprocess culture
 // we have set to German. The field will display the date/time using the "dd.mm.yyyy hh:mm" format.
 Assert.assertTrue(field.getResult().matches("\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}"));

 doc.getFieldOptions().setPreProcessCulture(new CultureInfo(Locale.ROOT));
 field.update();

 // After switching to the invariant culture, the DOCPROPERTY field will use the "mm/dd/yyyy hh:mm" format.
 Assert.assertTrue(field.getResult().matches("\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}"));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo/) | The culture to preprocess field values. |

### setResultFormatter(IFieldResultFormatter value) {#setResultFormatter-com.aspose.words.IFieldResultFormatter}
```
public void setResultFormatter(IFieldResultFormatter value)
```


Allows to control how the field result is formatted.

 **Examples:** 

Shows how to automatically apply a custom format to field results as the fields are updated.

```

 public void fieldResultFormatting() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     FieldResultFormatter formatter = new FieldResultFormatter("$%d", "Date: %tb", "Item # %s:");
     doc.getFieldOptions().setResultFormatter(formatter);

     // Our field result formatter applies a custom format to newly created fields of three types of formats.
     // Field result formatters apply new formatting to fields as they are updated,
     // which happens as soon as we create them using this InsertField method overload.
     // 1 -  Numeric:
     builder.insertField(" = 2 + 3 \\# $###");

     Assert.assertEquals("$5", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.NUMERIC));

     // 2 -  Date/time:
     builder.insertField("DATE \\@ \"d MMMM yyyy\"");

     Assert.assertTrue(doc.getRange().getFields().get(1).getResult().startsWith("Date: "));
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.DATE_TIME));

     // 3 -  General:
     builder.insertField("QUOTE \"2\" \\* Ordinal");

     Assert.assertEquals("Item # 2:", doc.getRange().getFields().get(2).getResult());
     Assert.assertEquals(1, formatter.countFormatInvocations(FieldResultFormatter.FormatInvocationType.GENERAL));

     formatter.printFormatInvocations();
 }

 /// 
 /// When fields with formatting are updated, this formatter will override their formatting
 /// with a custom format, while tracking every invocation.
 /// 
 private static class FieldResultFormatter implements IFieldResultFormatter {
     public FieldResultFormatter(String numberFormat, String dateFormat, String generalFormat) {
         mNumberFormat = numberFormat;
         mDateFormat = dateFormat;
         mGeneralFormat = generalFormat;
     }

     public String formatNumeric(double value, String format) {
         if (mNumberFormat.isEmpty())
             return null;

         String newValue = String.format(mNumberFormat, (long) value);
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.NUMERIC, value, format, newValue));
         return newValue;
     }

     public String formatDateTime(Date value, String format, int calendarType) {
         if (mDateFormat.isEmpty())
             return null;

         String newValue = String.format(mDateFormat, value);
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.DATE_TIME, MessageFormat.format("{0} ({1})", value, calendarType), format, newValue));
         return newValue;
     }

     public String format(String value, int format) {
         return format((Object) value, format);
     }

     public String format(double value, int format) {
         return format((Object) value, format);
     }

     private String format(Object value, int format) {
         if (mGeneralFormat.isEmpty())
             return null;

         String newValue = String.format(mGeneralFormat, new DecimalFormat("#.###").format(value));
         mFormatInvocations.add(new FormatInvocation(FormatInvocationType.GENERAL, value, GeneralFormat.toString(format), newValue));
         return newValue;
     }

     public int countFormatInvocations(int formatInvocationType) {
         if (formatInvocationType == FormatInvocationType.ALL)
             return getFormatInvocations().size();

         return (int) IterableUtils.countMatches(getFormatInvocations(), i -> i.getFormatInvocationType() == formatInvocationType);
     }

     public void printFormatInvocations() {
         for (FormatInvocation f : getFormatInvocations())
             System.out.println(MessageFormat.format("Invocation type:\t{0}\n" +
                     "\tOriginal value:\t\t{1}\n" +
                     "\tOriginal format:\t{2}\n" +
                     "\tNew value:\t\t\t{3}\n", f.getFormatInvocationType(), f.getValue(), f.getOriginalFormat(), f.getNewValue()));
     }

     private final String mNumberFormat;
     private final String mDateFormat;
     private final String mGeneralFormat;

     private ArrayList getFormatInvocations() {
         return mFormatInvocations;
     }

     private final ArrayList mFormatInvocations = new ArrayList<>();

     private static class FormatInvocation {
         public int getFormatInvocationType() {
             return mFormatInvocationType;
         }

         private final int mFormatInvocationType;

         public Object getValue() {
             return mValue;
         }

         private final Object mValue;

         public String getOriginalFormat() {
             return mOriginalFormat;
         }

         private final String mOriginalFormat;

         public String getNewValue() {
             return mNewValue;
         }

         private final String mNewValue;

         public FormatInvocation(int formatInvocationType, Object value, String originalFormat, String newValue) {
             mValue = value;
             mFormatInvocationType = formatInvocationType;
             mOriginalFormat = originalFormat;
             mNewValue = newValue;
         }
     }

     public final class FormatInvocationType {
         private FormatInvocationType() {
         }

         public static final int NUMERIC = 0;
         public static final int DATE_TIME = 1;
         public static final int GENERAL = 2;
         public static final int ALL = 3;

         public static final int length = 4;
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter/) | The corresponding [IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter/) value. |

### setTemplateName(String value) {#setTemplateName-java.lang.String}
```
public void setTemplateName(String value)
```


Sets the file name of the template used by the document.

 **Remarks:** 

This property is used by the [FieldTemplate](../../com.aspose.words/fieldtemplate/) field if the [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) property is empty.

If this property is empty, the default template file name  Normal.dotm  is used.

 **Examples:** 

Shows how to use a TEMPLATE field to display the local file system location of a document's template.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can set a template name using by the fields. This property is used when the "doc.AttachedTemplate" is empty.
 // If this property is empty the default template file name "Normal.dotm" is used.
 doc.getFieldOptions().setTemplateName("");

 FieldTemplate field = (FieldTemplate) builder.insertField(FieldType.FIELD_TEMPLATE, false);
 Assert.assertEquals(field.getFieldCode(), " TEMPLATE ");

 builder.writeln();
 field = (FieldTemplate) builder.insertField(FieldType.FIELD_TEMPLATE, false);
 field.setIncludeFullPath(true);

 Assert.assertEquals(field.getFieldCode(), " TEMPLATE  \\p");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TEMPLATE.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name of the template used by the document. |

### setToaCategories(ToaCategories value) {#setToaCategories-com.aspose.words.ToaCategories}
```
public void setToaCategories(ToaCategories value)
```


Sets the table of authorities categories.

 **Examples:** 

Shows how to specify a set of categories for TOA fields.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // TOA fields can filter their entries by categories defined in this collection.
 ToaCategories toaCategories = new ToaCategories();
 doc.getFieldOptions().setToaCategories(toaCategories);

 // This collection of categories comes with default values, which we can overwrite with custom values.
 Assert.assertEquals("Cases", toaCategories.get(1));
 Assert.assertEquals("Statutes", toaCategories.get(2));

 toaCategories.set(1, "My Category 1");
 toaCategories.set(2, "My Category 2");

 // We can always access the default values via this collection.
 Assert.assertEquals("Cases", ToaCategories.getDefaultCategories().get(1));
 Assert.assertEquals("Statutes", ToaCategories.getDefaultCategories().get(2));

 // Insert 2 TOA fields. TOA fields create an entry for each TA field in the document.
 // Use the "\c" switch to select the index of a category from our collection.
 //  With this switch, a TOA field will only pick up entries from TA fields that
 // also have a "\c" switch with a matching category index. Each TOA field will also display
 // the name of the category that its "\c" switch points to.
 builder.insertField("TOA \\c 1 \\h", null);
 builder.insertField("TOA \\c 2 \\h", null);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Insert TOA entries across 2 categories. Our first TOA field will receive one entry,
 // from the second TA field whose "\c" switch also points to the first category.
 // The second TOA field will have two entries from the other two TA fields.
 builder.insertField("TA \\c 2 \\l \"entry 1\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 1 \\l \"entry 2\"");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertField("TA \\c 2 \\l \"entry 3\"");

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.TOA.Categories.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [ToaCategories](../../com.aspose.words/toacategories/) | The table of authorities categories. |

### setUseInvariantCultureNumberFormat(boolean value) {#setUseInvariantCultureNumberFormat-boolean}
```
public void setUseInvariantCultureNumberFormat(boolean value)
```


Sets the value indicating that number format is parsed using invariant culture or not

 **Remarks:** 

When this property is set to  true , number format is taken from an invariant culture.

When this property is set to  false , number format is taken from the current thread's culture.

The default value is  false .

 **Examples:** 

Shows how to format numbers according to the invariant culture.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Locale.setDefault(new Locale("de-DE"));
 Field field = builder.insertField(" = 1234567,89 \\# $#,###,###.#");
 field.update();

 // Sometimes, fields may not format their numbers correctly under certain cultures.
 Assert.assertFalse(doc.getFieldOptions().getUseInvariantCultureNumberFormat());
 Assert.assertEquals("$123,456,789.  ", field.getResult());

 // To fix this, we could change the culture for the entire thread.
 // Another way to fix this is to set this flag,
 // which gets all fields to use the invariant culture when formatting numbers.
 // This way allows us to avoid changing the culture for the entire thread.
 doc.getFieldOptions().setUseInvariantCultureNumberFormat(true);
 field.update();
 Assert.assertEquals("$123,456,789.  ", field.getResult());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The value indicating that number format is parsed using invariant culture or not |

### setUserPromptRespondent(IFieldUserPromptRespondent value) {#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent}
```
public void setUserPromptRespondent(IFieldUserPromptRespondent value)
```


Sets the respondent to user prompts during field update.

 **Remarks:** 

If the value of this property is set to  null , the fields that require user response on prompting (such as [FieldAsk](../../com.aspose.words/fieldask/) or [FieldFillIn](../../com.aspose.words/fieldfillin/)) are not updated.

The default value is  null .

 **Examples:** 

Shows how to create an ASK field, and set its properties.

```

 public void fieldAsk() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Place a field where the response to our ASK field will be placed.
     FieldRef fieldRef = (FieldRef) builder.insertField(FieldType.FIELD_REF, true);
     fieldRef.setBookmarkName("MyAskField");
     builder.writeln();

     Assert.assertEquals(" REF  MyAskField", fieldRef.getFieldCode());

     // Insert the ASK field and edit its properties to reference our REF field by bookmark name.
     FieldAsk fieldAsk = (FieldAsk) builder.insertField(FieldType.FIELD_ASK, true);
     fieldAsk.setBookmarkName("MyAskField");
     fieldAsk.setPromptText("Please provide a response for this ASK field");
     fieldAsk.setDefaultResponse("Response from within the field.");
     fieldAsk.setPromptOnceOnMailMerge(true);
     builder.writeln();

     Assert.assertEquals(
             " ASK  MyAskField \"Please provide a response for this ASK field\" \\d \"Response from within the field.\" \\o",
             fieldAsk.getFieldCode());

     // ASK fields apply the default response to their respective REF fields during a mail merge.
     DataTable table = new DataTable("My Table");
     table.getColumns().add("Column 1");
     table.getRows().add("Row 1");
     table.getRows().add("Row 2");

     FieldMergeField fieldMergeField = (FieldMergeField) builder.insertField(FieldType.FIELD_MERGE_FIELD, true);
     fieldMergeField.setFieldName("Column 1");

     // We can modify or override the default response in our ASK fields with a custom prompt responder,
     // which will occur during a mail merge.
     doc.getFieldOptions().setUserPromptRespondent(new MyPromptRespondent());
     doc.getMailMerge().execute(table);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.ASK.docx");
 }

 /// 
 /// Prepends text to the default response of an ASK field during a mail merge.
 /// 
 private static class MyPromptRespondent implements IFieldUserPromptRespondent {
     public String respond(final String promptText, final String defaultResponse) {
         return "Response from MyPromptRespondent. " + defaultResponse;
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldUserPromptRespondent](../../com.aspose.words/ifielduserpromptrespondent/) | The respondent to user prompts during field update. |

