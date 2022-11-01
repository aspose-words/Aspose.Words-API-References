---
title: FieldOptions
second_title: Aspose.Words for Java API Reference
description: Represents options to control field handling in a document.
type: docs
weight: 227
url: /java/com.aspose.words/fieldoptions/
---

**Inheritance:**
java.lang.Object
```
public class FieldOptions
```

Represents options to control field handling in a document.

To learn more, visit the **Working with Fields** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBarcodeGenerator()](#getBarcodeGenerator--) | Gets or set custom barcode generator. |
| [getBuiltInTemplatesPaths()](#getBuiltInTemplatesPaths--) | Gets paths of MS Word built-in templates. |
| [getClass()](#getClass--) |  |
| [getComparisonExpressionEvaluator()](#getComparisonExpressionEvaluator--) | Gets the field comparison expressions evaluator. |
| [getCurrentUser()](#getCurrentUser--) | Gets the current user information. |
| [getCustomTocStyleSeparator()](#getCustomTocStyleSeparator--) | Gets custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc) field. |
| [getDefaultDocumentAuthor()](#getDefaultDocumentAuthor--) | Gets default document author's name. |
| [getFieldDatabaseProvider()](#getFieldDatabaseProvider--) | Gets a provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase) field. |
| [getFieldIndexFormat()](#getFieldIndexFormat--) | Gets a [getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex) fields in the document. |
| [getFieldUpdateCultureProvider()](#getFieldUpdateCultureProvider--) | Gets a provider that returns a culture object specific for each particular field. |
| [getFieldUpdateCultureSource()](#getFieldUpdateCultureSource--) | Specifies what culture to use to format the field result. |
| [getFieldUpdatingCallback()](#getFieldUpdatingCallback--) | Gets [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) implementation |
| [getFileName()](#getFileName--) | Gets the file name of the document. |
| [getLegacyNumberFormat()](#getLegacyNumberFormat--) | Gets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not. |
| [getPreProcessCulture()](#getPreProcessCulture--) | Gets the culture to preprocess field values. |
| [getResultFormatter()](#getResultFormatter--) | Allows to control how the field result is formatted. |
| [getTemplateName()](#getTemplateName--) | Gets the file name of the template used by the document. |
| [getToaCategories()](#getToaCategories--) | Gets the table of authorities categories. |
| [getUseInvariantCultureNumberFormat()](#getUseInvariantCultureNumberFormat--) | Gets the value indicating that number format is parsed using invariant culture or not |
| [getUserPromptRespondent()](#getUserPromptRespondent--) | Gets the respondent to user prompts during field update. |
| [hashCode()](#hashCode--) |  |
| [isBidiTextSupportedOnUpdate()](#isBidiTextSupportedOnUpdate--) | Gets the value indicating whether bidirectional text is fully supported during field update or not. |
| [isBidiTextSupportedOnUpdate(boolean value)](#isBidiTextSupportedOnUpdate-boolean-) | Sets the value indicating whether bidirectional text is fully supported during field update or not. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBarcodeGenerator(IBarcodeGenerator value)](#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator-) | Gets or set custom barcode generator. |
| [setBuiltInTemplatesPaths(String[] value)](#setBuiltInTemplatesPaths-java.lang.String---) | Sets paths of MS Word built-in templates. |
| [setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value)](#setComparisonExpressionEvaluator-com.aspose.words.IComparisonExpressionEvaluator-) | Sets the field comparison expressions evaluator. |
| [setCurrentUser(UserInformation value)](#setCurrentUser-com.aspose.words.UserInformation-) | Sets the current user information. |
| [setCustomTocStyleSeparator(String value)](#setCustomTocStyleSeparator-java.lang.String-) | Sets custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc) field. |
| [setDefaultDocumentAuthor(String value)](#setDefaultDocumentAuthor-java.lang.String-) | Sets default document author's name. |
| [setFieldDatabaseProvider(IFieldDatabaseProvider value)](#setFieldDatabaseProvider-com.aspose.words.IFieldDatabaseProvider-) | Sets a provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase) field. |
| [setFieldIndexFormat(int value)](#setFieldIndexFormat-int-) | Sets a [getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex) fields in the document. |
| [setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value)](#setFieldUpdateCultureProvider-com.aspose.words.IFieldUpdateCultureProvider-) | Sets a provider that returns a culture object specific for each particular field. |
| [setFieldUpdateCultureSource(int value)](#setFieldUpdateCultureSource-int-) | Specifies what culture to use to format the field result. |
| [setFieldUpdatingCallback(IFieldUpdatingCallback value)](#setFieldUpdatingCallback-com.aspose.words.IFieldUpdatingCallback-) | Sets [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) implementation |
| [setFileName(String value)](#setFileName-java.lang.String-) | Sets the file name of the document. |
| [setLegacyNumberFormat(boolean value)](#setLegacyNumberFormat-boolean-) | Sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not. |
| [setPreProcessCulture(System.Globalization.CultureInfo value)](#setPreProcessCulture-com.aspose.words.net.System.Globalization.CultureInfo-) | Sets the culture to preprocess field values. |
| [setResultFormatter(IFieldResultFormatter value)](#setResultFormatter-com.aspose.words.IFieldResultFormatter-) | Allows to control how the field result is formatted. |
| [setTemplateName(String value)](#setTemplateName-java.lang.String-) | Sets the file name of the template used by the document. |
| [setToaCategories(ToaCategories value)](#setToaCategories-com.aspose.words.ToaCategories-) | Sets the table of authorities categories. |
| [setUseInvariantCultureNumberFormat(boolean value)](#setUseInvariantCultureNumberFormat-boolean-) | Sets the value indicating that number format is parsed using invariant culture or not |
| [setUserPromptRespondent(IFieldUserPromptRespondent value)](#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent-) | Sets the respondent to user prompts during field update. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getBarcodeGenerator() {#getBarcodeGenerator--}
```
public IBarcodeGenerator getBarcodeGenerator()
```


Gets or set custom barcode generator. Custom barcode generator should implement public interface [IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator).

**Returns:**
[IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator) - Or set custom barcode generator.
### getBuiltInTemplatesPaths() {#getBuiltInTemplatesPaths--}
```
public String[] getBuiltInTemplatesPaths()
```


Gets paths of MS Word built-in templates.

This property is used by the [FieldAutoText](../../com.aspose.words/fieldautotext) and [FieldGlossary](../../com.aspose.words/fieldglossary) fields, if referenced auto text entry is not found in the [Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) template.

By default MS Word stores built-in templates in c:\\Users\\\\AppData\\Roaming\\Microsoft\\Document Building Blocks\\1033\\16\\Built-In Building Blocks.dotx and C:\\Users\\\\AppData\\Roaming\\Microsoft\\Templates\\Normal.dotm files.

**Returns:**
java.lang.String[] - Paths of MS Word built-in templates.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getComparisonExpressionEvaluator() {#getComparisonExpressionEvaluator--}
```
public IComparisonExpressionEvaluator getComparisonExpressionEvaluator()
```


Gets the field comparison expressions evaluator.

**Returns:**
[IComparisonExpressionEvaluator](../../com.aspose.words/icomparisonexpressionevaluator) - The field comparison expressions evaluator.
### getCurrentUser() {#getCurrentUser--}
```
public UserInformation getCurrentUser()
```


Gets the current user information.

**Returns:**
[UserInformation](../../com.aspose.words/userinformation) - The current user information.
### getCustomTocStyleSeparator() {#getCustomTocStyleSeparator--}
```
public String getCustomTocStyleSeparator()
```


Gets custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc) field. By default, custom styles defined by the \\t switch in the [FieldToc](../../com.aspose.words/fieldtoc) field are separated by a delimiter taken from the current culture. This property overrides that behaviour by specifying a user defined delimiter.

**Returns:**
java.lang.String - Custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc) field.
### getDefaultDocumentAuthor() {#getDefaultDocumentAuthor--}
```
public String getDefaultDocumentAuthor()
```


Gets default document author's name. If author's name is already specified in built-in document properties, this option is not considered.

**Returns:**
java.lang.String - Default document author's name.
### getFieldDatabaseProvider() {#getFieldDatabaseProvider--}
```
public IFieldDatabaseProvider getFieldDatabaseProvider()
```


Gets a provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase) field.

**Returns:**
[IFieldDatabaseProvider](../../com.aspose.words/ifielddatabaseprovider) - A provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase) field.
### getFieldIndexFormat() {#getFieldIndexFormat--}
```
public int getFieldIndexFormat()
```


Gets a [getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex) fields in the document.

**Returns:**
int - A [getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex) fields in the document. The returned value is one of [FieldIndexFormat](../../com.aspose.words/fieldindexformat) constants.
### getFieldUpdateCultureProvider() {#getFieldUpdateCultureProvider--}
```
public IFieldUpdateCultureProvider getFieldUpdateCultureProvider()
```


Gets a provider that returns a culture object specific for each particular field.

The provider is requested when the value of [getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-) is **FieldUpdateCultureSource.FieldCode**.

If the provider is present, then the culture object it returns is used for the field update. Otherwise, a system culture is used.

**Returns:**
[IFieldUpdateCultureProvider](../../com.aspose.words/ifieldupdatecultureprovider) - A provider that returns a culture object specific for each particular field.
### getFieldUpdateCultureSource() {#getFieldUpdateCultureSource--}
```
public int getFieldUpdateCultureSource()
```


Specifies what culture to use to format the field result.

By default, the culture of the current thread is used.

The setting affects only date/time fields with \\\\@ format switch.

**Returns:**
int - The corresponding  int  value. The returned value is one of [FieldUpdateCultureSource](../../com.aspose.words/fieldupdateculturesource) constants.
### getFieldUpdatingCallback() {#getFieldUpdatingCallback--}
```
public IFieldUpdatingCallback getFieldUpdatingCallback()
```


Gets [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) implementation

**Returns:**
[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) - \{[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) implementation
### getFileName() {#getFileName--}
```
public String getFileName()
```


Gets the file name of the document.

This property is used by the [FieldFileName](../../com.aspose.words/fieldfilename) field with higher priority than the [Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--) property.

**Returns:**
java.lang.String - The file name of the document.
### getLegacyNumberFormat() {#getLegacyNumberFormat--}
```
public boolean getLegacyNumberFormat()
```


Gets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not.

When this property is set to **true**, template symbol "\#" worked as in .net: Replaces the pound sign with the corresponding digit if one is present; otherwise, no symbols appears in the result string.

When this property is set to **false**, template symbol "\#" works as MS Word: This format item specifies the requisite numeric places to display in the result. If the result does not include a digit in that place, MS Word displays a space. For example, \{ = 9 + 6 \\\# $\#\#\# \} displays $ 15.

The default value is **false**.

**Returns:**
boolean - The value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not.
### getPreProcessCulture() {#getPreProcessCulture--}
```
public System.Globalization.CultureInfo getPreProcessCulture()
```


Gets the culture to preprocess field values.

Currently this property only affects value of the [FieldDocProperty](../../com.aspose.words/fielddocproperty) field.

The default value is **null**. When this property is set to **null**, the [FieldDocProperty](../../com.aspose.words/fielddocproperty) field's value is preprocessed with the culture controlled by the [getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-) property.

**Returns:**
[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) - The culture to preprocess field values.
### getResultFormatter() {#getResultFormatter--}
```
public IFieldResultFormatter getResultFormatter()
```


Allows to control how the field result is formatted.

**Returns:**
[IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter) - The corresponding [IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter) value.
### getTemplateName() {#getTemplateName--}
```
public String getTemplateName()
```


Gets the file name of the template used by the document.

This property is used by the [FieldTemplate](../../com.aspose.words/fieldtemplate) field if the [Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) property is empty.

If this property is empty, the default template file name  Normal.dotm  is used.

**Returns:**
java.lang.String - The file name of the template used by the document.
### getToaCategories() {#getToaCategories--}
```
public ToaCategories getToaCategories()
```


Gets the table of authorities categories.

**Returns:**
[ToaCategories](../../com.aspose.words/toacategories) - The table of authorities categories.
### getUseInvariantCultureNumberFormat() {#getUseInvariantCultureNumberFormat--}
```
public boolean getUseInvariantCultureNumberFormat()
```


Gets the value indicating that number format is parsed using invariant culture or not

When this property is set to **true**, number format is taken from an invariant culture.

When this property is set to **false**, number format is taken from the current thread's culture.

The default value is **false**.

**Returns:**
boolean - The value indicating that number format is parsed using invariant culture or not
### getUserPromptRespondent() {#getUserPromptRespondent--}
```
public IFieldUserPromptRespondent getUserPromptRespondent()
```


Gets the respondent to user prompts during field update.

If the value of this property is set to **null**, the fields that require user response on prompting (such as [FieldAsk](../../com.aspose.words/fieldask) or [FieldFillIn](../../com.aspose.words/fieldfillin)) are not updated.

The default value is **null**.

**Returns:**
[IFieldUserPromptRespondent](../../com.aspose.words/ifielduserpromptrespondent) - The respondent to user prompts during field update.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isBidiTextSupportedOnUpdate() {#isBidiTextSupportedOnUpdate--}
```
public boolean isBidiTextSupportedOnUpdate()
```


Gets the value indicating whether bidirectional text is fully supported during field update or not.

When this property is set to **true**, additional steps are performed to produce Right-To-Left language (i.e. Arabic or Hebrew) compatible field result during its update.

When this property is set to **false** and Right-To-Left language is used, correctness of field result after its update is not guaranteed.

The default value is **false**.

**Returns:**
boolean - The value indicating whether bidirectional text is fully supported during field update or not.
### isBidiTextSupportedOnUpdate(boolean value) {#isBidiTextSupportedOnUpdate-boolean-}
```
public void isBidiTextSupportedOnUpdate(boolean value)
```


Sets the value indicating whether bidirectional text is fully supported during field update or not.

When this property is set to **true**, additional steps are performed to produce Right-To-Left language (i.e. Arabic or Hebrew) compatible field result during its update.

When this property is set to **false** and Right-To-Left language is used, correctness of field result after its update is not guaranteed.

The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The value indicating whether bidirectional text is fully supported during field update or not. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setBarcodeGenerator(IBarcodeGenerator value) {#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator-}
```
public void setBarcodeGenerator(IBarcodeGenerator value)
```


Gets or set custom barcode generator. Custom barcode generator should implement public interface [IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator) | Or set custom barcode generator. |

### setBuiltInTemplatesPaths(String[] value) {#setBuiltInTemplatesPaths-java.lang.String---}
```
public void setBuiltInTemplatesPaths(String[] value)
```


Sets paths of MS Word built-in templates.

This property is used by the [FieldAutoText](../../com.aspose.words/fieldautotext) and [FieldGlossary](../../com.aspose.words/fieldglossary) fields, if referenced auto text entry is not found in the [Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) template.

By default MS Word stores built-in templates in c:\\Users\\\\AppData\\Roaming\\Microsoft\\Document Building Blocks\\1033\\16\\Built-In Building Blocks.dotx and C:\\Users\\\\AppData\\Roaming\\Microsoft\\Templates\\Normal.dotm files.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String[] | Paths of MS Word built-in templates. |

### setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value) {#setComparisonExpressionEvaluator-com.aspose.words.IComparisonExpressionEvaluator-}
```
public void setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value)
```


Sets the field comparison expressions evaluator.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IComparisonExpressionEvaluator](../../com.aspose.words/icomparisonexpressionevaluator) | The field comparison expressions evaluator. |

### setCurrentUser(UserInformation value) {#setCurrentUser-com.aspose.words.UserInformation-}
```
public void setCurrentUser(UserInformation value)
```


Sets the current user information.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [UserInformation](../../com.aspose.words/userinformation) | The current user information. |

### setCustomTocStyleSeparator(String value) {#setCustomTocStyleSeparator-java.lang.String-}
```
public void setCustomTocStyleSeparator(String value)
```


Sets custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc) field. By default, custom styles defined by the \\t switch in the [FieldToc](../../com.aspose.words/fieldtoc) field are separated by a delimiter taken from the current culture. This property overrides that behaviour by specifying a user defined delimiter.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Custom style separator for the \\t switch in [FieldToc](../../com.aspose.words/fieldtoc) field. |

### setDefaultDocumentAuthor(String value) {#setDefaultDocumentAuthor-java.lang.String-}
```
public void setDefaultDocumentAuthor(String value)
```


Sets default document author's name. If author's name is already specified in built-in document properties, this option is not considered.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Default document author's name. |

### setFieldDatabaseProvider(IFieldDatabaseProvider value) {#setFieldDatabaseProvider-com.aspose.words.IFieldDatabaseProvider-}
```
public void setFieldDatabaseProvider(IFieldDatabaseProvider value)
```


Sets a provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase) field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldDatabaseProvider](../../com.aspose.words/ifielddatabaseprovider) | A provider that returns a query result for the [FieldDatabase](../../com.aspose.words/fielddatabase) field. |

### setFieldIndexFormat(int value) {#setFieldIndexFormat-int-}
```
public void setFieldIndexFormat(int value)
```


Sets a [getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex) fields in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A [getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) that represents the formatting for the [FieldIndex](../../com.aspose.words/fieldindex) fields in the document. The value must be one of [FieldIndexFormat](../../com.aspose.words/fieldindexformat) constants. |

### setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value) {#setFieldUpdateCultureProvider-com.aspose.words.IFieldUpdateCultureProvider-}
```
public void setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value)
```


Sets a provider that returns a culture object specific for each particular field.

The provider is requested when the value of [getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-) is **FieldUpdateCultureSource.FieldCode**.

If the provider is present, then the culture object it returns is used for the field update. Otherwise, a system culture is used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldUpdateCultureProvider](../../com.aspose.words/ifieldupdatecultureprovider) | A provider that returns a culture object specific for each particular field. |

### setFieldUpdateCultureSource(int value) {#setFieldUpdateCultureSource-int-}
```
public void setFieldUpdateCultureSource(int value)
```


Specifies what culture to use to format the field result.

By default, the culture of the current thread is used.

The setting affects only date/time fields with \\\\@ format switch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FieldUpdateCultureSource](../../com.aspose.words/fieldupdateculturesource) constants. |

### setFieldUpdatingCallback(IFieldUpdatingCallback value) {#setFieldUpdatingCallback-com.aspose.words.IFieldUpdatingCallback-}
```
public void setFieldUpdatingCallback(IFieldUpdatingCallback value)
```


Sets [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) implementation

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) | \{[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) implementation |

### setFileName(String value) {#setFileName-java.lang.String-}
```
public void setFileName(String value)
```


Sets the file name of the document.

This property is used by the [FieldFileName](../../com.aspose.words/fieldfilename) field with higher priority than the [Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--) property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name of the document. |

### setLegacyNumberFormat(boolean value) {#setLegacyNumberFormat-boolean-}
```
public void setLegacyNumberFormat(boolean value)
```


Sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not.

When this property is set to **true**, template symbol "\#" worked as in .net: Replaces the pound sign with the corresponding digit if one is present; otherwise, no symbols appears in the result string.

When this property is set to **false**, template symbol "\#" works as MS Word: This format item specifies the requisite numeric places to display in the result. If the result does not include a digit in that place, MS Word displays a space. For example, \{ = 9 + 6 \\\# $\#\#\# \} displays $ 15.

The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not. |

### setPreProcessCulture(System.Globalization.CultureInfo value) {#setPreProcessCulture-com.aspose.words.net.System.Globalization.CultureInfo-}
```
public void setPreProcessCulture(System.Globalization.CultureInfo value)
```


Sets the culture to preprocess field values.

Currently this property only affects value of the [FieldDocProperty](../../com.aspose.words/fielddocproperty) field.

The default value is **null**. When this property is set to **null**, the [FieldDocProperty](../../com.aspose.words/fielddocproperty) field's value is preprocessed with the culture controlled by the [getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-) property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) | The culture to preprocess field values. |

### setResultFormatter(IFieldResultFormatter value) {#setResultFormatter-com.aspose.words.IFieldResultFormatter-}
```
public void setResultFormatter(IFieldResultFormatter value)
```


Allows to control how the field result is formatted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter) | The corresponding [IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter) value. |

### setTemplateName(String value) {#setTemplateName-java.lang.String-}
```
public void setTemplateName(String value)
```


Sets the file name of the template used by the document.

This property is used by the [FieldTemplate](../../com.aspose.words/fieldtemplate) field if the [Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) property is empty.

If this property is empty, the default template file name  Normal.dotm  is used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name of the template used by the document. |

### setToaCategories(ToaCategories value) {#setToaCategories-com.aspose.words.ToaCategories-}
```
public void setToaCategories(ToaCategories value)
```


Sets the table of authorities categories.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [ToaCategories](../../com.aspose.words/toacategories) | The table of authorities categories. |

### setUseInvariantCultureNumberFormat(boolean value) {#setUseInvariantCultureNumberFormat-boolean-}
```
public void setUseInvariantCultureNumberFormat(boolean value)
```


Sets the value indicating that number format is parsed using invariant culture or not

When this property is set to **true**, number format is taken from an invariant culture.

When this property is set to **false**, number format is taken from the current thread's culture.

The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The value indicating that number format is parsed using invariant culture or not |

### setUserPromptRespondent(IFieldUserPromptRespondent value) {#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent-}
```
public void setUserPromptRespondent(IFieldUserPromptRespondent value)
```


Sets the respondent to user prompts during field update.

If the value of this property is set to **null**, the fields that require user response on prompting (such as [FieldAsk](../../com.aspose.words/fieldask) or [FieldFillIn](../../com.aspose.words/fieldfillin)) are not updated.

The default value is **null**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFieldUserPromptRespondent](../../com.aspose.words/ifielduserpromptrespondent) | The respondent to user prompts during field update. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

