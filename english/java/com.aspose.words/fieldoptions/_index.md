---
title: 字段Options
second_title: Aspose.Words for Java API 参考
description: 表示用于控制文档中的字段处理的选项。
type: docs
weight: 227
url: /zh/java/com.aspose.words/fieldoptions/
---

**遗产:**
java.lang.Object
```
public class 字段Options
```

表示用于控制文档中的字段处理的选项。

要了解更多信息，请访问**Working with 字段**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBarcodeGenerator()](#getBarcodeGenerator--) | 获取或设置自定义条码生成器。 |
| [getBuiltInTemplatesPaths()](#getBuiltInTemplatesPaths--) | 获取 MS Word 内置模板的路径。 |
| [get班级()](#get班级--) |  |
| [getComparisonExpressionEvaluator()](#getComparisonExpressionEvaluator--) | 获取字段比较表达式计算器。 |
| [getCurrentUser()](#getCurrentUser--) | 获取当前用户信息。 |
| [getCustomTocStyleSeparator()](#getCustomTocStyleSeparator--) | 获取自定义样式分隔符\\t 切换[字段Toc](../../com.aspose.words/fieldtoc)场地。 |
| [getDefaultDocumentAuthor()](#getDefaultDocumentAuthor--) | 获取默认文档作者的姓名。 |
| [get字段DatabaseProvider()](#get字段DatabaseProvider--) | 获取返回查询结果的提供程序[字段Database](../../com.aspose.words/fielddatabase)场地。 |
| [get字段IndexFormat()](#get字段IndexFormat--) | 得到一个[get字段IndexFormat()](../../com.aspose.words/fieldoptions\#get字段IndexFormat--) / [set字段IndexFormat(int)](../../com.aspose.words/fieldoptions\#set字段IndexFormat-int-)表示格式的[字段Index](../../com.aspose.words/fieldindex)文档中的字段。 |
| [get字段UpdateCultureProvider()](#get字段UpdateCultureProvider--) | 获取返回特定于每个特定字段的区域性对象的提供程序。 |
| [get字段UpdateCultureSource()](#get字段UpdateCultureSource--) | 指定用于格式化字段结果的区域性。 |
| [get字段UpdatingCallback()](#get字段UpdatingCallback--) | 获取[I字段UpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行 |
| [getFileName()](#getFileName--) | 获取文档的文件名。 |
| [getLegacyNumberFormat()](#getLegacyNumberFormat--) | 获取指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。 |
| [getPreProcessCulture()](#getPreProcessCulture--) | 获取区域性以预处理字段值。 |
| [getResultFormatter()](#getResultFormatter--) | 允许控制字段结果的格式。 |
| [getTemplateName()](#getTemplateName--) | 获取文档使用的模板的文件名。 |
| [getToaCategories()](#getToaCategories--) | 获取权限类别表。 |
| [getUseInvariantCultureNumberFormat()](#getUseInvariantCultureNumberFormat--) | 获取表示数字格式是否使用不变区域性解析的值 |
| [getUserPromptRespondent()](#getUserPromptRespondent--) | 在字段更新期间获取用户提示的响应者。 |
| [hashCode()](#hashCode--) |  |
| [isBidiTextSupportedOnUpdate()](#isBidiTextSupportedOnUpdate--) | 获取指示在字段更新期间是否完全支持双向文本的值。 |
| [isBidiTextSupportedOnUpdate(boolean value)](#isBidiTextSupportedOnUpdate-boolean-) | 设置指示在字段更新期间是否完全支持双向文本的值。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBarcodeGenerator(IBarcodeGenerator value)](#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator-) | 获取或设置自定义条码生成器。 |
| [setBuiltInTemplatesPaths(String[] value)](#setBuiltInTemplatesPaths-java.lang.String---) | 设置 MS Word 内置模板的路径。 |
| [setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value)](#setComparisonExpressionEvaluator-com.aspose.words.IComparisonExpressionEvaluator-) | 设置字段比较表达式计算器。 |
| [setCurrentUser(UserInformation value)](#setCurrentUser-com.aspose.words.UserInformation-) | 设置当前用户信息。 |
| [setCustomTocStyleSeparator(String value)](#setCustomTocStyleSeparator-java.lang.String-) | 设置自定义样式分隔符\\t 切换[字段Toc](../../com.aspose.words/fieldtoc)场地。 |
| [setDefaultDocumentAuthor(String value)](#setDefaultDocumentAuthor-java.lang.String-) | 设置默认文档作者的姓名。 |
| [set字段DatabaseProvider(I字段DatabaseProvider value)](#set字段DatabaseProvider-com.aspose.words.I字段DatabaseProvider-) | 设置返回查询结果的提供程序[字段Database](../../com.aspose.words/fielddatabase)场地。 |
| [set字段IndexFormat(int value)](#set字段IndexFormat-int-) | 设置一个[get字段IndexFormat()](../../com.aspose.words/fieldoptions\#get字段IndexFormat--) / [set字段IndexFormat(int)](../../com.aspose.words/fieldoptions\#set字段IndexFormat-int-)表示格式的[字段Index](../../com.aspose.words/fieldindex)文档中的字段。 |
| [set字段UpdateCultureProvider(I字段UpdateCultureProvider value)](#set字段UpdateCultureProvider-com.aspose.words.I字段UpdateCultureProvider-) | 设置一个提供程序，该提供程序返回特定于每个特定字段的区域性对象。 |
| [set字段UpdateCultureSource(int value)](#set字段UpdateCultureSource-int-) | 指定用于格式化字段结果的区域性。 |
| [set字段UpdatingCallback(I字段UpdatingCallback value)](#set字段UpdatingCallback-com.aspose.words.I字段UpdatingCallback-) | 套[I字段UpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行 |
| [setFileName(String value)](#setFileName-java.lang.String-) | 设置文档的文件名。 |
| [setLegacyNumberFormat(boolean value)](#setLegacyNumberFormat-boolean-) | 设置指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。 |
| [setPreProcessCulture(System.Globalization.CultureInfo value)](#setPreProcessCulture-com.aspose.words.net.System.Globalization.CultureInfo-) | 将区域性设置为预处理字段值。 |
| [setResultFormatter(I字段ResultFormatter value)](#setResultFormatter-com.aspose.words.I字段ResultFormatter-) | 允许控制字段结果的格式。 |
| [setTemplateName(String value)](#setTemplateName-java.lang.String-) | 设置文档使用的模板的文件名。 |
| [setToaCategories(ToaCategories value)](#setToaCategories-com.aspose.words.ToaCategories-) | 设置权限类别表。 |
| [setUseInvariantCultureNumberFormat(boolean value)](#setUseInvariantCultureNumberFormat-boolean-) | 设置指示数字格式是否使用不变区域性解析的值 |
| [setUserPromptRespondent(I字段UserPromptRespondent value)](#setUserPromptRespondent-com.aspose.words.I字段UserPromptRespondent-) | 在字段更新期间将响应者设置为用户提示。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getBarcodeGenerator() {#getBarcodeGenerator--}
```
public IBarcodeGenerator getBarcodeGenerator()
```


获取或设置自定义条码生成器。自定义条码生成器应实现公共接口[IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator).

**退货:**
[IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator) 或设置自定义条码生成器。
### getBuiltInTemplatesPaths() {#getBuiltInTemplatesPaths--}
```
public String[] getBuiltInTemplatesPaths()
```


获取 MS Word 内置模板的路径。

该属性由[字段AutoText](../../com.aspose.words/fieldautotext)和[字段Glossary](../../com.aspose.words/fieldglossary)字段，如果在[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)模板。

默认情况下，MS Word 将内置模板存储在 c 中：\\用户\\\\应用程序数据\\漫游\\微软\\文档构建块\\1033\\16\\内置 Building Blocks.dotx 和 C：\\用户\\\\应用程序数据\\漫游\\微软\\模板\\Normal.dotm 文件。

**退货:**
java.lang.String[] - MS Word 内置模板的路径。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getComparisonExpressionEvaluator() {#getComparisonExpressionEvaluator--}
```
public IComparisonExpressionEvaluator getComparisonExpressionEvaluator()
```


获取字段比较表达式计算器。

**退货:**
[IComparisonExpressionEvaluator](../../com.aspose.words/icomparisonexpressionevaluator) - 字段比较表达式评估器。
### getCurrentUser() {#getCurrentUser--}
```
public UserInformation getCurrentUser()
```


获取当前用户信息。

**退货:**
[UserInformation](../../com.aspose.words/userinformation) - 当前用户信息。
### getCustomTocStyleSeparator() {#getCustomTocStyleSeparator--}
```
public String getCustomTocStyleSeparator()
```


获取自定义样式分隔符\\t 切换[字段Toc](../../com.aspose.words/fieldtoc)场地。默认情况下，由\\t 切换[字段Toc](../../com.aspose.words/fieldtoc)字段由取自当前区域性的分隔符分隔。此属性通过指定用户定义的分隔符来覆盖该行为。

**退货:**
 java.lang.String - 自定义样式分隔符\\t 切换[字段Toc](../../com.aspose.words/fieldtoc)场地。
### getDefaultDocumentAuthor() {#getDefaultDocumentAuthor--}
```
public String getDefaultDocumentAuthor()
```


获取默认文档作者的姓名。如果已在内置文档属性中指定作者姓名，则不考虑此选项。

**退货:**
java.lang.String - 默认文档作者的姓名。
### get字段DatabaseProvider() {#get字段DatabaseProvider--}
```
public I字段DatabaseProvider get字段DatabaseProvider()
```


获取返回查询结果的提供程序[字段Database](../../com.aspose.words/fielddatabase)场地。

**退货:**
[I字段DatabaseProvider](../../com.aspose.words/ifielddatabaseprovider) - 返回查询结果的提供程序[字段Database](../../com.aspose.words/fielddatabase)场地。
### get字段IndexFormat() {#get字段IndexFormat--}
```
public int get字段IndexFormat()
```


得到一个[get字段IndexFormat()](../../com.aspose.words/fieldoptions\#get字段IndexFormat--) / [set字段IndexFormat(int)](../../com.aspose.words/fieldoptions\#set字段IndexFormat-int-)表示格式的[字段Index](../../com.aspose.words/fieldindex)文档中的字段。

**退货:**
诠释 - A[get字段IndexFormat()](../../com.aspose.words/fieldoptions\#get字段IndexFormat--) / [set字段IndexFormat(int)](../../com.aspose.words/fieldoptions\#set字段IndexFormat-int-)表示格式的[字段Index](../../com.aspose.words/fieldindex)文档中的字段。返回值是以下之一[字段IndexFormat](../../com.aspose.words/fieldindexformat)常数。
### get字段UpdateCultureProvider() {#get字段UpdateCultureProvider--}
```
public I字段UpdateCultureProvider get字段UpdateCultureProvider()
```


获取返回特定于每个特定字段的区域性对象的提供程序。

当值为[get字段UpdateCultureSource()](../../com.aspose.words/fieldoptions\#get字段UpdateCultureSource--) / [set字段UpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#set字段UpdateCultureSource-int-)是**字段UpdateCultureSource.字段Code**.

如果提供者存在，则它返回的区域性对象用于字段更新。否则，使用系统文化。

**退货:**
[I字段UpdateCultureProvider](../../com.aspose.words/ifieldupdatecultureprovider) - 返回特定于每个特定字段的文化对象的提供程序。
### get字段UpdateCultureSource() {#get字段UpdateCultureSource--}
```
public int get字段UpdateCultureSource()
```


指定用于格式化字段结果的区域性。

默认情况下，使用当前线程的文化。

该设置仅影响日期/时间字段\\\\@ 格式切换。

**退货:**
int - 对应的 int 值。返回值是以下之一[字段UpdateCultureSource](../../com.aspose.words/fieldupdateculturesource)常数。
### get字段UpdatingCallback() {#get字段UpdatingCallback--}
```
public I字段UpdatingCallback get字段UpdatingCallback()
```


获取[I字段UpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行

**退货:**
[I字段UpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) -\{[I字段UpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行
### getFileName() {#getFileName--}
```
public String getFileName()
```


获取文档的文件名。

该属性由[字段FileName](../../com.aspose.words/fieldfilename)具有更高优先级的字段[Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--)财产。

**退货:**
java.lang.String - 文档的文件名。
### getLegacyNumberFormat() {#getLegacyNumberFormat--}
```
public boolean getLegacyNumberFormat()
```


获取指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。

当此属性设置为**true**模板符号 "\#" 在 .net 中工作：如果存在，则将井号替换为相应的数字；否则，结果字符串中不会出现符号。

当此属性设置为**false**模板符号 "\ #" 作为 MS Word 工作：此格式项指定要在结果中显示的必要数字位置。如果结果在该位置不包含数字，MS Word 将显示一个空格。例如，\ { = 9 + 6\\\ #$\#\#\# \} 显示 15 美元。

默认值为**false**.

**退货:**
boolean - 指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。
### getPreProcessCulture() {#getPreProcessCulture--}
```
public System.Globalization.CultureInfo getPreProcessCulture()
```


获取区域性以预处理字段值。

目前这个属性只影响[字段DocProperty](../../com.aspose.words/fielddocproperty)场地。

默认值为**null**.当此属性设置为**null**， 这[字段DocProperty](../../com.aspose.words/fielddocproperty)字段的值使用受控制的区域性进行预处理[get字段UpdateCultureSource()](../../com.aspose.words/fieldoptions\#get字段UpdateCultureSource--) / [set字段UpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#set字段UpdateCultureSource-int-)财产。

**退货:**
[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) 预处理字段值的文化。
### getResultFormatter() {#getResultFormatter--}
```
public I字段ResultFormatter getResultFormatter()
```


允许控制字段结果的格式。

**退货:**
[I字段ResultFormatter](../../com.aspose.words/ifieldresultformatter) - 相应的[I字段ResultFormatter](../../com.aspose.words/ifieldresultformatter)价值。
### getTemplateName() {#getTemplateName--}
```
public String getTemplateName()
```


获取文档使用的模板的文件名。

该属性由[字段Template](../../com.aspose.words/fieldtemplate)字段如果[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)属性为空。

如果此属性为空，则使用默认模板文件名 Normal.dotm。

**退货:**
java.lang.String - 文档使用的模板的文件名。
### getToaCategories() {#getToaCategories--}
```
public ToaCategories getToaCategories()
```


获取权限类别表。

**退货:**
[ToaCategories](../../com.aspose.words/toacategories) 权限类别表。
### getUseInvariantCultureNumberFormat() {#getUseInvariantCultureNumberFormat--}
```
public boolean getUseInvariantCultureNumberFormat()
```


获取表示数字格式是否使用不变区域性解析的值

当此属性设置为**true**, 数字格式取自不变的文化。

当此属性设置为**false**, 数字格式取自当前线程的文化。

默认值为**false**.

**退货:**
boolean - 指示数字格式是否使用不变文化解析的值
### getUserPromptRespondent() {#getUserPromptRespondent--}
```
public I字段UserPromptRespondent getUserPromptRespondent()
```


在字段更新期间获取用户提示的响应者。

如果此属性的值设置为**null**，需要用户响应提示的字段（例如[字段Ask](../../com.aspose.words/fieldask)或者[字段FillIn](../../com.aspose.words/fieldfillin)不更新。

默认值为**null**.

**退货:**
[I字段UserPromptRespondent](../../com.aspose.words/ifielduserpromptrespondent) - 字段更新期间用户提示的受访者。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isBidiTextSupportedOnUpdate() {#isBidiTextSupportedOnUpdate--}
```
public boolean isBidiTextSupportedOnUpdate()
```


获取指示在字段更新期间是否完全支持双向文本的值。

当此属性设置为**true**，执行附加步骤以在其更新期间生成从右到左的语言（即阿拉伯语或希伯来语）兼容的字段结果。

当此属性设置为**false**并且使用从右到左的语言，不保证更新后字段结果的正确性。

默认值为**false**.

**退货:**
boolean - 指示在字段更新期间是否完全支持双向文本的值。
### isBidiTextSupportedOnUpdate(boolean value) {#isBidiTextSupportedOnUpdate-boolean-}
```
public void isBidiTextSupportedOnUpdate(boolean value)
```


设置指示在字段更新期间是否完全支持双向文本的值。

当此属性设置为**true**，执行附加步骤以在其更新期间生成从右到左的语言（即阿拉伯语或希伯来语）兼容的字段结果。

当此属性设置为**false**并且使用从右到左的语言，不保证更新后字段结果的正确性。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示在字段更新期间是否完全支持双向文本的值。 |

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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator) | 或设置自定义条码生成器。 |

### setBuiltInTemplatesPaths(String[] value) {#setBuiltInTemplatesPaths-java.lang.String---}
```
public void setBuiltInTemplatesPaths(String[] value)
```


设置 MS Word 内置模板的路径。

该属性由[字段AutoText](../../com.aspose.words/fieldautotext)和[字段Glossary](../../com.aspose.words/fieldglossary)字段，如果在[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)模板。

默认情况下，MS Word 将内置模板存储在 c 中：\\用户\\\\应用程序数据\\漫游\\微软\\文档构建块\\1033\\16\\内置 Building Blocks.dotx 和 C：\\用户\\\\应用程序数据\\漫游\\微软\\模板\\Normal.dotm 文件。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String[] | MS Word 内置模板的路径。 |

### setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value) {#setComparisonExpressionEvaluator-com.aspose.words.IComparisonExpressionEvaluator-}
```
public void setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value)
```


设置字段比较表达式计算器。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IComparisonExpressionEvaluator](../../com.aspose.words/icomparisonexpressionevaluator) | 字段比较表达式求值器。 |

### setCurrentUser(UserInformation value) {#setCurrentUser-com.aspose.words.UserInformation-}
```
public void setCurrentUser(UserInformation value)
```


设置当前用户信息。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [UserInformation](../../com.aspose.words/userinformation) | 当前用户信息。 |

### setCustomTocStyleSeparator(String value) {#setCustomTocStyleSeparator-java.lang.String-}
```
public void setCustomTocStyleSeparator(String value)
```


设置自定义样式分隔符\\t 切换[字段Toc](../../com.aspose.words/fieldtoc)场地。默认情况下，由\\t 切换[字段Toc](../../com.aspose.words/fieldtoc)字段由取自当前区域性的分隔符分隔。此属性通过指定用户定义的分隔符来覆盖该行为。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 自定义样式分隔符\\t 切换[字段Toc](../../com.aspose.words/fieldtoc)场地。 |

### setDefaultDocumentAuthor(String value) {#setDefaultDocumentAuthor-java.lang.String-}
```
public void setDefaultDocumentAuthor(String value)
```


设置默认文档作者的姓名。如果已在内置文档属性中指定作者姓名，则不考虑此选项。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 默认文档作者姓名。 |

### set字段DatabaseProvider(I字段DatabaseProvider value) {#set字段DatabaseProvider-com.aspose.words.I字段DatabaseProvider-}
```
public void set字段DatabaseProvider(I字段DatabaseProvider value)
```


设置返回查询结果的提供程序[字段Database](../../com.aspose.words/fielddatabase)场地。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [I字段DatabaseProvider](../../com.aspose.words/ifielddatabaseprovider) | 返回查询结果的提供程序[字段Database](../../com.aspose.words/fielddatabase)场地。 |

### set字段IndexFormat(int value) {#set字段IndexFormat-int-}
```
public void set字段IndexFormat(int value)
```


设置一个[get字段IndexFormat()](../../com.aspose.words/fieldoptions\#get字段IndexFormat--) / [set字段IndexFormat(int)](../../com.aspose.words/fieldoptions\#set字段IndexFormat-int-)表示格式的[字段Index](../../com.aspose.words/fieldindex)文档中的字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 一个[get字段IndexFormat()](../../com.aspose.words/fieldoptions\#get字段IndexFormat--) / [set字段IndexFormat(int)](../../com.aspose.words/fieldoptions\#set字段IndexFormat-int-)表示格式的[字段Index](../../com.aspose.words/fieldindex)文档中的字段。该值必须是以下之一[字段IndexFormat](../../com.aspose.words/fieldindexformat)常数。 |

### set字段UpdateCultureProvider(I字段UpdateCultureProvider value) {#set字段UpdateCultureProvider-com.aspose.words.I字段UpdateCultureProvider-}
```
public void set字段UpdateCultureProvider(I字段UpdateCultureProvider value)
```


设置一个提供程序，该提供程序返回特定于每个特定字段的区域性对象。

当值为[get字段UpdateCultureSource()](../../com.aspose.words/fieldoptions\#get字段UpdateCultureSource--) / [set字段UpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#set字段UpdateCultureSource-int-)是**字段UpdateCultureSource.字段Code**.

如果提供者存在，则它返回的区域性对象用于字段更新。否则，使用系统文化。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [I字段UpdateCultureProvider](../../com.aspose.words/ifieldupdatecultureprovider) | 返回特定于每个特定字段的区域性对象的提供程序。 |

### set字段UpdateCultureSource(int value) {#set字段UpdateCultureSource-int-}
```
public void set字段UpdateCultureSource(int value)
```


指定用于格式化字段结果的区域性。

默认情况下，使用当前线程的文化。

该设置仅影响日期/时间字段\\\\@ 格式切换。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[字段UpdateCultureSource](../../com.aspose.words/fieldupdateculturesource)常数。 |

### set字段UpdatingCallback(I字段UpdatingCallback value) {#set字段UpdatingCallback-com.aspose.words.I字段UpdatingCallback-}
```
public void set字段UpdatingCallback(I字段UpdatingCallback value)
```


套[I字段UpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [I字段UpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) | \{[I字段UpdatingCallback](../../com.aspose.words/ifieldupdatingcallback)执行 |

### setFileName(String value) {#setFileName-java.lang.String-}
```
public void setFileName(String value)
```


设置文档的文件名。

该属性由[字段FileName](../../com.aspose.words/fieldfilename)具有更高优先级的字段[Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--)财产。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档的文件名。 |

### setLegacyNumberFormat(boolean value) {#setLegacyNumberFormat-boolean-}
```
public void setLegacyNumberFormat(boolean value)
```


设置指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。

当此属性设置为**true**模板符号 "\#" 在 .net 中工作：如果存在，则将井号替换为相应的数字；否则，结果字符串中不会出现符号。

当此属性设置为**false**模板符号 "\ #" 作为 MS Word 工作：此格式项指定要在结果中显示的必要数字位置。如果结果在该位置不包含数字，MS Word 将显示一个空格。例如，\ { = 9 + 6\\\ #$\#\#\# \} 显示 15 美元。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。 |

### setPreProcessCulture(System.Globalization.CultureInfo value) {#setPreProcessCulture-com.aspose.words.net.System.Globalization.CultureInfo-}
```
public void setPreProcessCulture(System.Globalization.CultureInfo value)
```


将区域性设置为预处理字段值。

目前这个属性只影响[字段DocProperty](../../com.aspose.words/fielddocproperty)场地。

默认值为**null**.当此属性设置为**null**， 这[字段DocProperty](../../com.aspose.words/fielddocproperty)字段的值使用受控制的区域性进行预处理[get字段UpdateCultureSource()](../../com.aspose.words/fieldoptions\#get字段UpdateCultureSource--) / [set字段UpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#set字段UpdateCultureSource-int-)财产。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) | 预处理字段值的文化。 |

### setResultFormatter(I字段ResultFormatter value) {#setResultFormatter-com.aspose.words.I字段ResultFormatter-}
```
public void setResultFormatter(I字段ResultFormatter value)
```


允许控制字段结果的格式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [I字段ResultFormatter](../../com.aspose.words/ifieldresultformatter) | 相应的[I字段ResultFormatter](../../com.aspose.words/ifieldresultformatter)价值。 |

### setTemplateName(String value) {#setTemplateName-java.lang.String-}
```
public void setTemplateName(String value)
```


设置文档使用的模板的文件名。

该属性由[字段Template](../../com.aspose.words/fieldtemplate)字段如果[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)属性为空。

如果此属性为空，则使用默认模板文件名 Normal.dotm。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档使用的模板的文件名。 |

### setToaCategories(ToaCategories value) {#setToaCategories-com.aspose.words.ToaCategories-}
```
public void setToaCategories(ToaCategories value)
```


设置权限类别表。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [ToaCategories](../../com.aspose.words/toacategories) | 权限类别表。 |

### setUseInvariantCultureNumberFormat(boolean value) {#setUseInvariantCultureNumberFormat-boolean-}
```
public void setUseInvariantCultureNumberFormat(boolean value)
```


设置指示数字格式是否使用不变区域性解析的值

当此属性设置为**true**, 数字格式取自不变的文化。

当此属性设置为**false**, 数字格式取自当前线程的文化。

默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示数字格式是否使用不变区域性解析的值 |

### setUserPromptRespondent(I字段UserPromptRespondent value) {#setUserPromptRespondent-com.aspose.words.I字段UserPromptRespondent-}
```
public void setUserPromptRespondent(I字段UserPromptRespondent value)
```


在字段更新期间将响应者设置为用户提示。

如果此属性的值设置为**null**，需要用户响应提示的字段（例如[字段Ask](../../com.aspose.words/fieldask)或者[字段FillIn](../../com.aspose.words/fieldfillin)不更新。

默认值为**null**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [I字段UserPromptRespondent](../../com.aspose.words/ifielduserpromptrespondent) | 字段更新期间用户提示的被访者。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
