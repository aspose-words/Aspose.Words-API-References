---
title: FieldOptions
second_title: Aspose.Words for Java API 参考
description: 表示控制文档中字段处理的选项。
type: docs
weight: 227
url: /zh/java/com.aspose.words/fieldoptions/
---

**遗产：**
java.lang.Object
```
public class FieldOptions
```

表示控制文档中字段处理的选项。

要了解更多信息，请访问**Working with Fields**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBarcodeGenerator()](#getBarcodeGenerator--) | 获取或设置自定义条码生成器。 |
| [getBuiltInTemplatesPaths()](#getBuiltInTemplatesPaths--) | 获取 MS Word 内置模板的路径。 |
| [getClass()](#getClass--) |  |
| [getComparisonExpressionEvaluator()](#getComparisonExpressionEvaluator--) | 获取字段比较表达式求值器。 |
| [getCurrentUser()](#getCurrentUser--) | 获取当前用户信息。 |
| [getCustomTocStyleSeparator()](#getCustomTocStyleSeparator--) | 获取自定义样式分隔符\\t 切换[FieldToc](../../com.aspose.words/fieldtoc)场地。 |
| [getDefaultDocumentAuthor()](#getDefaultDocumentAuthor--) | 获取默认文档作者的姓名。 |
| [getFieldDatabaseProvider()](#getFieldDatabaseProvider--) | 获取返回查询结果的提供程序[FieldDatabase](../../com.aspose.words/fielddatabase)场地。 |
| [getFieldIndexFormat()](#getFieldIndexFormat--) | 得到一个[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-)表示格式的[FieldIndex](../../com.aspose.words/fieldindex)文档中的字段。 |
| [getFieldUpdateCultureProvider()](#getFieldUpdateCultureProvider--) | 获取返回特定于每个特定字段的区域性对象的提供程序。 |
| [getFieldUpdateCultureSource()](#getFieldUpdateCultureSource--) | 指定用于格式化字段结果的区域性。 |
| [getFieldUpdatingCallback()](#getFieldUpdatingCallback--) | 得到[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行 |
| [getFileName()](#getFileName--) | 获取文档的文件名。 |
| [getLegacyNumberFormat()](#getLegacyNumberFormat--) | 获取指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。 |
| [getPreProcessCulture()](#getPreProcessCulture--) | 获取文化以预处理字段值。 |
| [getResultFormatter()](#getResultFormatter--) | 允许控制字段结果的格式。 |
| [getTemplateName()](#getTemplateName--) | 获取文档使用的模板的文件名。 |
| [getToaCategories()](#getToaCategories--) | 获取权限类别表。 |
| [getUseInvariantCultureNumberFormat()](#getUseInvariantCultureNumberFormat--) | 获取表示是否使用不变区域性解析数字格式的值 |
| [getUserPromptRespondent()](#getUserPromptRespondent--) | 在字段更新期间获取用户提示的响应者。 |
| [hashCode()](#hashCode--) |  |
| [isBidiTextSupportedOnUpdate()](#isBidiTextSupportedOnUpdate--) | 获取指示在字段更新期间是否完全支持双向文本的值。 |
| [isBidiTextSupportedOnUpdate(boolean value)](#isBidiTextSupportedOnUpdate-boolean-) | 设置指示在字段更新期间是否完全支持双向文本的值。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBarcodeGenerator(IBarcodeGenerator value)](#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator-) | 获取或设置自定义条码生成器。 |
| [setBuiltInTemplatesPaths(String[] value)](#setBuiltInTemplatesPaths-java.lang.String---) | 设置 MS Word 内置模板的路径。 |
| [setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value)](#setComparisonExpressionEvaluator-com.aspose.words.IComparisonExpressionEvaluator-) | 设置字段比较表达式求值器。 |
| [setCurrentUser(UserInformation value)](#setCurrentUser-com.aspose.words.UserInformation-) | 设置当前用户信息。 |
| [setCustomTocStyleSeparator(String value)](#setCustomTocStyleSeparator-java.lang.String-) | 为\\t 切换[FieldToc](../../com.aspose.words/fieldtoc)场地。 |
| [setDefaultDocumentAuthor(String value)](#setDefaultDocumentAuthor-java.lang.String-) | 设置默认文档作者的姓名。 |
| [setFieldDatabaseProvider(IFieldDatabaseProvider value)](#setFieldDatabaseProvider-com.aspose.words.IFieldDatabaseProvider-) | 设置返回查询结果的提供者[FieldDatabase](../../com.aspose.words/fielddatabase)场地。 |
| [setFieldIndexFormat(int value)](#setFieldIndexFormat-int-) | 设置一个[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-)表示格式的[FieldIndex](../../com.aspose.words/fieldindex)文档中的字段。 |
| [setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value)](#setFieldUpdateCultureProvider-com.aspose.words.IFieldUpdateCultureProvider-) | 设置一个提供程序，该提供程序返回特定于每个特定字段的文化对象。 |
| [setFieldUpdateCultureSource(int value)](#setFieldUpdateCultureSource-int-) | 指定用于格式化字段结果的区域性。 |
| [setFieldUpdatingCallback(IFieldUpdatingCallback value)](#setFieldUpdatingCallback-com.aspose.words.IFieldUpdatingCallback-) | 套[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行 |
| [setFileName(String value)](#setFileName-java.lang.String-) | 设置文档的文件名。 |
| [setLegacyNumberFormat(boolean value)](#setLegacyNumberFormat-boolean-) | 设置指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。 |
| [setPreProcessCulture(System.Globalization.CultureInfo value)](#setPreProcessCulture-com.aspose.words.net.System.Globalization.CultureInfo-) | 将区域性设置为预处理字段值。 |
| [setResultFormatter(IFieldResultFormatter value)](#setResultFormatter-com.aspose.words.IFieldResultFormatter-) | 允许控制字段结果的格式。 |
| [setTemplateName(String value)](#setTemplateName-java.lang.String-) | 设置文档使用的模板的文件名。 |
| [setToaCategories(ToaCategories value)](#setToaCategories-com.aspose.words.ToaCategories-) | 设置权限类别表。 |
| [setUseInvariantCultureNumberFormat(boolean value)](#setUseInvariantCultureNumberFormat-boolean-) | 设置指示是否使用不变区域性解析数字格式的值 |
| [setUserPromptRespondent(IFieldUserPromptRespondent value)](#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent-) | 在字段更新期间将响应者设置为用户提示。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getBarcodeGenerator() {#getBarcodeGenerator--}
```
public IBarcodeGenerator getBarcodeGenerator()
```


获取或设置自定义条码生成器。自定义条码生成器应实现公共接口[IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator).

**退货：**
[IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator) 或设置自定义条码生成器。
### getBuiltInTemplatesPaths() {#getBuiltInTemplatesPaths--}
```
public String[] getBuiltInTemplatesPaths()
```


获取 MS Word 内置模板的路径。

该属性由[FieldAutoText](../../com.aspose.words/fieldautotext)和[FieldGlossary](../../com.aspose.words/fieldglossary)字段，如果在[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)模板。

默认情况下，MS Word 将内置模板存储在 c:\\用户\\\\应用程序数据\\漫游\\微软\\文档构建块\\1033\\16\\Built-In Building Blocks.dotx 和 C:\\用户\\\\应用程序数据\\漫游\\微软\\模板\\Normal.dotm 文件。

**退货：**
java.lang.字符串[] - MS Word 内置模板的路径。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getComparisonExpressionEvaluator() {#getComparisonExpressionEvaluator--}
```
public IComparisonExpressionEvaluator getComparisonExpressionEvaluator()
```


获取字段比较表达式求值器。

**退货：**
[IComparisonExpressionEvaluator](../../com.aspose.words/icomparisonexpressionevaluator) - 字段比较表达式求值器。
### getCurrentUser() {#getCurrentUser--}
```
public UserInformation getCurrentUser()
```


获取当前用户信息。

**退货：**
[UserInformation](../../com.aspose.words/userinformation) - 当前用户信息。
### getCustomTocStyleSeparator() {#getCustomTocStyleSeparator--}
```
public String getCustomTocStyleSeparator()
```


获取自定义样式分隔符\\t 切换[FieldToc](../../com.aspose.words/fieldtoc)场地。默认情况下，自定义样式由\\t 切换[FieldToc](../../com.aspose.words/fieldtoc)字段由取自当前区域性的定界符分隔。此属性通过指定用户定义的定界符来覆盖该行为。

**退货：**
 java.lang.String - 的自定义样式分隔符\\t 切换[FieldToc](../../com.aspose.words/fieldtoc)场地。
### getDefaultDocumentAuthor() {#getDefaultDocumentAuthor--}
```
public String getDefaultDocumentAuthor()
```


获取默认文档作者的姓名。如果内置文档属性中已指定作者姓名，则不考虑此选项。

**退货：**
java.lang.String - 默认文档作者的姓名。
### getFieldDatabaseProvider() {#getFieldDatabaseProvider--}
```
public IFieldDatabaseProvider getFieldDatabaseProvider()
```


获取返回查询结果的提供程序[FieldDatabase](../../com.aspose.words/fielddatabase)场地。

**退货：**
[IFieldDatabaseProvider](../../com.aspose.words/ifielddatabaseprovider) - 返回查询结果的提供者[FieldDatabase](../../com.aspose.words/fielddatabase)场地。
### getFieldIndexFormat() {#getFieldIndexFormat--}
```
public int getFieldIndexFormat()
```


得到一个[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-)表示格式的[FieldIndex](../../com.aspose.words/fieldindex)文档中的字段。

**退货：**
诠释 - A[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-)表示格式的[FieldIndex](../../com.aspose.words/fieldindex)文档中的字段。返回值是其中之一[FieldIndexFormat](../../com.aspose.words/fieldindexformat)常数。
### getFieldUpdateCultureProvider() {#getFieldUpdateCultureProvider--}
```
public IFieldUpdateCultureProvider getFieldUpdateCultureProvider()
```


获取返回特定于每个特定字段的区域性对象的提供程序。

提供者被请求时的值[getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-)是**FieldUpdateCultureSource.FieldCode**.

如果提供程序存在，则它返回的区域性对象用于字段更新。否则，将使用系统文化。

**退货：**
[IFieldUpdateCultureProvider](../../com.aspose.words/ifieldupdatecultureprovider) - 返回特定于每个特定字段的文化对象的提供者。
### getFieldUpdateCultureSource() {#getFieldUpdateCultureSource--}
```
public int getFieldUpdateCultureSource()
```


指定用于格式化字段结果的区域性。

默认情况下，使用当前线程的文化。

该设置仅影响日期/时间字段\\\\@ 格式开关。

**退货：**
int - 相应的 int 值。返回值是其中之一[FieldUpdateCultureSource](../../com.aspose.words/fieldupdateculturesource)常数。
### getFieldUpdatingCallback() {#getFieldUpdatingCallback--}
```
public IFieldUpdatingCallback getFieldUpdatingCallback()
```


得到[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行

**退货：**
[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) -\{[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行
### getFileName() {#getFileName--}
```
public String getFileName()
```


获取文档的文件名。

该属性由[FieldFileName](../../com.aspose.words/fieldfilename)优先级高于[Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--)财产。

**退货：**
java.lang.String - 文档的文件名。
### getLegacyNumberFormat() {#getLegacyNumberFormat--}
```
public boolean getLegacyNumberFormat()
```


获取指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。

当此属性设置为**true**模板符号 "\#" 在 .net 中的工作方式：如果存在井号，则将井号替换为相应的数字；否则，结果字符串中不会出现任何符号。

当此属性设置为**false**模板符号 "\ #" works as MS Word：此格式项指定要在结果中显示的必要数字位置。如果结果在该位置不包含数字，MS Word 将显示一个空格。例如，\ { = 9 + 6\\\ #$\#\#\# \} 显示 $15。

默认值为**false**.

**退货：**
boolean - 指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。
### getPreProcessCulture() {#getPreProcessCulture--}
```
public System.Globalization.CultureInfo getPreProcessCulture()
```


获取文化以预处理字段值。

目前此属性仅影响的值[FieldDocProperty](../../com.aspose.words/fielddocproperty)场地。

默认值为**null**.当此属性设置为**null**， 这[FieldDocProperty](../../com.aspose.words/fielddocproperty)字段的值是用由控制的文化预处理的[getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-)财产。

**退货：**
[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) 预处理字段值的文化。
### getResultFormatter() {#getResultFormatter--}
```
public IFieldResultFormatter getResultFormatter()
```


允许控制字段结果的格式。

**退货：**
[IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter) - 相应的[IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter)价值。
### getTemplateName() {#getTemplateName--}
```
public String getTemplateName()
```


获取文档使用的模板的文件名。

该属性由[FieldTemplate](../../com.aspose.words/fieldtemplate)字段如果[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)属性为空。

如果此属性为空，则使用默认模板文件名 Normal.dotm。

**退货：**
java.lang.String - 文档使用的模板的文件名。
### getToaCategories() {#getToaCategories--}
```
public ToaCategories getToaCategories()
```


获取权限类别表。

**退货：**
[ToaCategories](../../com.aspose.words/toacategories) 权限类别表。
### getUseInvariantCultureNumberFormat() {#getUseInvariantCultureNumberFormat--}
```
public boolean getUseInvariantCultureNumberFormat()
```


获取表示是否使用不变区域性解析数字格式的值

当此属性设置为**true**，数字格式取自不变的文化。

当此属性设置为**false**，数字格式取自当前线程的文化。

默认值为**false**.

**退货：**
boolean - 指示数字格式是否使用不变区域性解析的值
### getUserPromptRespondent() {#getUserPromptRespondent--}
```
public IFieldUserPromptRespondent getUserPromptRespondent()
```


在字段更新期间获取用户提示的响应者。

如果此属性的值设置为**null**，需要用户响应提示的字段（例如[FieldAsk](../../com.aspose.words/fieldask)或者[FieldFillIn](../../com.aspose.words/fieldfillin)未更新。

默认值为**null**.

**退货：**
[IFieldUserPromptRespondent](../../com.aspose.words/ifielduserpromptrespondent) - 字段更新期间用户提示的响应者。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### isBidiTextSupportedOnUpdate() {#isBidiTextSupportedOnUpdate--}
```
public boolean isBidiTextSupportedOnUpdate()
```


获取指示在字段更新期间是否完全支持双向文本的值。

当此属性设置为**true**, 执行额外的步骤以在其更新期间生成从右到左的语言（即阿拉伯语或希伯来语）兼容的字段结果。

当此属性设置为**false**并且使用从右到左的语言，不保证字段结果更新后的正确性。

默认值为**false**.

**退货：**
boolean - 指示在字段更新期间是否完全支持双向文本的值。
### isBidiTextSupportedOnUpdate(boolean value) {#isBidiTextSupportedOnUpdate-boolean-}
```
public void isBidiTextSupportedOnUpdate(boolean value)
```


设置指示在字段更新期间是否完全支持双向文本的值。

当此属性设置为**true**, 执行额外的步骤以在其更新期间生成从右到左的语言（即阿拉伯语或希伯来语）兼容的字段结果。

当此属性设置为**false**并且使用从右到左的语言，不保证字段结果更新后的正确性。

默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 该值指示在字段更新期间是否完全支持双向文本。 |

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


获取或设置自定义条码生成器。自定义条码生成器应实现公共接口[IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator) | 或设置自定义条码生成器。 |

### setBuiltInTemplatesPaths(String[] value) {#setBuiltInTemplatesPaths-java.lang.String---}
```
public void setBuiltInTemplatesPaths(String[] value)
```


设置 MS Word 内置模板的路径。

该属性由[FieldAutoText](../../com.aspose.words/fieldautotext)和[FieldGlossary](../../com.aspose.words/fieldglossary)字段，如果在[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)模板。

默认情况下，MS Word 将内置模板存储在 c:\\用户\\\\应用程序数据\\漫游\\微软\\文档构建块\\1033\\16\\Built-In Building Blocks.dotx 和 C:\\用户\\\\应用程序数据\\漫游\\微软\\模板\\Normal.dotm 文件。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String[] | MS Word 内置模板的路径。 |

### setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value) {#setComparisonExpressionEvaluator-com.aspose.words.IComparisonExpressionEvaluator-}
```
public void setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value)
```


设置字段比较表达式求值器。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IComparisonExpressionEvaluator](../../com.aspose.words/icomparisonexpressionevaluator) | 字段比较表达式求值器。 |

### setCurrentUser(UserInformation value) {#setCurrentUser-com.aspose.words.UserInformation-}
```
public void setCurrentUser(UserInformation value)
```


设置当前用户信息。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [UserInformation](../../com.aspose.words/userinformation) | 当前用户信息。 |

### setCustomTocStyleSeparator(String value) {#setCustomTocStyleSeparator-java.lang.String-}
```
public void setCustomTocStyleSeparator(String value)
```


为\\t 切换[FieldToc](../../com.aspose.words/fieldtoc)场地。默认情况下，自定义样式由\\t 切换[FieldToc](../../com.aspose.words/fieldtoc)字段由取自当前区域性的定界符分隔。此属性通过指定用户定义的定界符来覆盖该行为。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 的自定义样式分隔符\\t 切换[FieldToc](../../com.aspose.words/fieldtoc)场地。 |

### setDefaultDocumentAuthor(String value) {#setDefaultDocumentAuthor-java.lang.String-}
```
public void setDefaultDocumentAuthor(String value)
```


设置默认文档作者的姓名。如果内置文档属性中已指定作者姓名，则不考虑此选项。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 默认文档作者的姓名。 |

### setFieldDatabaseProvider(IFieldDatabaseProvider value) {#setFieldDatabaseProvider-com.aspose.words.IFieldDatabaseProvider-}
```
public void setFieldDatabaseProvider(IFieldDatabaseProvider value)
```


设置返回查询结果的提供者[FieldDatabase](../../com.aspose.words/fielddatabase)场地。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IFieldDatabaseProvider](../../com.aspose.words/ifielddatabaseprovider) | 返回查询结果的提供程序[FieldDatabase](../../com.aspose.words/fielddatabase)场地。 |

### setFieldIndexFormat(int value) {#setFieldIndexFormat-int-}
```
public void setFieldIndexFormat(int value)
```


设置一个[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-)表示格式的[FieldIndex](../../com.aspose.words/fieldindex)文档中的字段。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 一个[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-)表示格式的[FieldIndex](../../com.aspose.words/fieldindex)文档中的字段。该值必须是其中之一[FieldIndexFormat](../../com.aspose.words/fieldindexformat)常数。 |

### setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value) {#setFieldUpdateCultureProvider-com.aspose.words.IFieldUpdateCultureProvider-}
```
public void setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value)
```


设置一个提供程序，该提供程序返回特定于每个特定字段的文化对象。

提供者被请求时的值[getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-)是**FieldUpdateCultureSource.FieldCode**.

如果提供程序存在，则它返回的区域性对象用于字段更新。否则，将使用系统文化。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IFieldUpdateCultureProvider](../../com.aspose.words/ifieldupdatecultureprovider) | 返回特定于每个特定字段的区域性对象的提供程序。 |

### setFieldUpdateCultureSource(int value) {#setFieldUpdateCultureSource-int-}
```
public void setFieldUpdateCultureSource(int value)
```


指定用于格式化字段结果的区域性。

默认情况下，使用当前线程的文化。

该设置仅影响日期/时间字段\\\\@ 格式开关。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[FieldUpdateCultureSource](../../com.aspose.words/fieldupdateculturesource)常数。 |

### setFieldUpdatingCallback(IFieldUpdatingCallback value) {#setFieldUpdatingCallback-com.aspose.words.IFieldUpdatingCallback-}
```
public void setFieldUpdatingCallback(IFieldUpdatingCallback value)
```


套[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) | \{[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行 |

### setFileName(String value) {#setFileName-java.lang.String-}
```
public void setFileName(String value)
```


设置文档的文件名。

该属性由[FieldFileName](../../com.aspose.words/fieldfilename)优先级高于[Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--)财产。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档的文件名。 |

### setLegacyNumberFormat(boolean value) {#setLegacyNumberFormat-boolean-}
```
public void setLegacyNumberFormat(boolean value)
```


设置指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。

当此属性设置为**true**模板符号 "\#" 在 .net 中的工作方式：如果存在井号，则将井号替换为相应的数字；否则，结果字符串中不会出现任何符号。

当此属性设置为**false**模板符号 "\ #" works as MS Word：此格式项指定要在结果中显示的必要数字位置。如果结果在该位置不包含数字，MS Word 将显示一个空格。例如，\ { = 9 + 6\\\ #$\#\#\# \} 显示 $15。

默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 该值指示是否启用字段的旧版（早于 AW 13.10）数字格式。 |

### setPreProcessCulture(System.Globalization.CultureInfo value) {#setPreProcessCulture-com.aspose.words.net.System.Globalization.CultureInfo-}
```
public void setPreProcessCulture(System.Globalization.CultureInfo value)
```


将区域性设置为预处理字段值。

目前此属性仅影响的值[FieldDocProperty](../../com.aspose.words/fielddocproperty)场地。

默认值为**null**.当此属性设置为**null**， 这[FieldDocProperty](../../com.aspose.words/fielddocproperty)字段的值是用由控制的文化预处理的[getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-)财产。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) | 预处理字段值的区域性。 |

### setResultFormatter(IFieldResultFormatter value) {#setResultFormatter-com.aspose.words.IFieldResultFormatter-}
```
public void setResultFormatter(IFieldResultFormatter value)
```


允许控制字段结果的格式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter) | 相应的[IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter)价值。 |

### setTemplateName(String value) {#setTemplateName-java.lang.String-}
```
public void setTemplateName(String value)
```


设置文档使用的模板的文件名。

该属性由[FieldTemplate](../../com.aspose.words/fieldtemplate)字段如果[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)属性为空。

如果此属性为空，则使用默认模板文件名 Normal.dotm。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档使用的模板的文件名。 |

### setToaCategories(ToaCategories value) {#setToaCategories-com.aspose.words.ToaCategories-}
```
public void setToaCategories(ToaCategories value)
```


设置权限类别表。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [ToaCategories](../../com.aspose.words/toacategories) | 权限类别表。 |

### setUseInvariantCultureNumberFormat(boolean value) {#setUseInvariantCultureNumberFormat-boolean-}
```
public void setUseInvariantCultureNumberFormat(boolean value)
```


设置指示是否使用不变区域性解析数字格式的值

当此属性设置为**true**，数字格式取自不变的文化。

当此属性设置为**false**，数字格式取自当前线程的文化。

默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 表示数字格式是否使用不变文化解析的值 |

### setUserPromptRespondent(IFieldUserPromptRespondent value) {#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent-}
```
public void setUserPromptRespondent(IFieldUserPromptRespondent value)
```


在字段更新期间将响应者设置为用户提示。

如果此属性的值设置为**null**，需要用户响应提示的字段（例如[FieldAsk](../../com.aspose.words/fieldask)或者[FieldFillIn](../../com.aspose.words/fieldfillin)未更新。

默认值为**null**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IFieldUserPromptRespondent](../../com.aspose.words/ifielduserpromptrespondent) | 字段更新期间用户提示的响应者。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
