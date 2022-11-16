---
title: FieldOptions
second_title: Справочник по API Aspose.Words для Java
description: Представляет параметры для управления обработкой полей в документе.
type: docs
weight: 227
url: /ru/java/com.aspose.words/fieldoptions/
---

**Наследование:**
java.lang.Object
```
public class FieldOptions
```

Представляет параметры для управления обработкой полей в документе.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBarcodeGenerator()](#getBarcodeGenerator--) | Получает или задает пользовательский генератор штрих-кода. |
| [getBuiltInTemplatesPaths()](#getBuiltInTemplatesPaths--) | Получает пути к встроенным шаблонам MS Word. |
| [getClass()](#getClass--) |  |
| [getComparisonExpressionEvaluator()](#getComparisonExpressionEvaluator--) | Получает средство оценки выражений сравнения полей. |
| [getCurrentUser()](#getCurrentUser--) | Получает информацию о текущем пользователе. |
| [getCustomTocStyleSeparator()](#getCustomTocStyleSeparator--) | Получает разделитель пользовательского стиля для\ \t включить[FieldToc](../../com.aspose.words/fieldtoc) поле. |
| [getDefaultDocumentAuthor()](#getDefaultDocumentAuthor--) | Получает имя автора документа по умолчанию. |
| [getFieldDatabaseProvider()](#getFieldDatabaseProvider--) |  Получает поставщика, который возвращает результат запроса для[FieldDatabase](../../com.aspose.words/fielddatabase) поле. |
| [getFieldIndexFormat()](#getFieldIndexFormat--) | Получает[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) который представляет форматирование для[FieldIndex](../../com.aspose.words/fieldindex) поля в документе. |
| [getFieldUpdateCultureProvider()](#getFieldUpdateCultureProvider--) | Получает поставщика, возвращающего объект культуры для каждого конкретного поля. |
| [getFieldUpdateCultureSource()](#getFieldUpdateCultureSource--) | Указывает, какую культуру использовать для форматирования результата поля. |
| [getFieldUpdatingCallback()](#getFieldUpdatingCallback--) |  Получает[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) реализация |
| [getFileName()](#getFileName--) | Получает имя файла документа. |
| [getLegacyNumberFormat()](#getLegacyNumberFormat--) | Получает значение, указывающее, включен ли устаревший (более ранний, чем AW 13.10) числовой формат для полей. |
| [getPreProcessCulture()](#getPreProcessCulture--) | Получает культуру для предварительной обработки значений поля. |
| [getResultFormatter()](#getResultFormatter--) | Позволяет управлять форматированием результата поля. |
| [getTemplateName()](#getTemplateName--) | Получает имя файла шаблона, используемого документом. |
| [getToaCategories()](#getToaCategories--) | Получает таблицу категорий полномочий. |
| [getUseInvariantCultureNumberFormat()](#getUseInvariantCultureNumberFormat--) | Получает значение, указывающее, анализируется ли числовой формат с использованием инвариантного языка и региональных параметров. |
| [getUserPromptRespondent()](#getUserPromptRespondent--) | Получает респондента на запросы пользователя во время обновления поля. |
| [hashCode()](#hashCode--) |  |
| [isBidiTextSupportedOnUpdate()](#isBidiTextSupportedOnUpdate--) | Получает значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля. |
| [isBidiTextSupportedOnUpdate(boolean value)](#isBidiTextSupportedOnUpdate-boolean-) | Задает значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBarcodeGenerator(IBarcodeGenerator value)](#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator-) | Получает или задает пользовательский генератор штрих-кода. |
| [setBuiltInTemplatesPaths(String[] value)](#setBuiltInTemplatesPaths-java.lang.String---) | Задает пути к встроенным шаблонам MS Word. |
| [setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value)](#setComparisonExpressionEvaluator-com.aspose.words.IComparisonExpressionEvaluator-) | Устанавливает оценщик выражений сравнения полей. |
| [setCurrentUser(UserInformation value)](#setCurrentUser-com.aspose.words.UserInformation-) | Устанавливает текущую информацию о пользователе. |
| [setCustomTocStyleSeparator(String value)](#setCustomTocStyleSeparator-java.lang.String-) |  Устанавливает разделитель пользовательского стиля для\ \t включить[FieldToc](../../com.aspose.words/fieldtoc) поле. |
| [setDefaultDocumentAuthor(String value)](#setDefaultDocumentAuthor-java.lang.String-) | Устанавливает имя автора документа по умолчанию. |
| [setFieldDatabaseProvider(IFieldDatabaseProvider value)](#setFieldDatabaseProvider-com.aspose.words.IFieldDatabaseProvider-) |  Задает поставщика, который возвращает результат запроса для[FieldDatabase](../../com.aspose.words/fielddatabase) поле. |
| [setFieldIndexFormat(int value)](#setFieldIndexFormat-int-) |  Устанавливает[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) который представляет форматирование для[FieldIndex](../../com.aspose.words/fieldindex) поля в документе. |
| [setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value)](#setFieldUpdateCultureProvider-com.aspose.words.IFieldUpdateCultureProvider-) | Задает поставщика, который возвращает объект культуры для каждого конкретного поля. |
| [setFieldUpdateCultureSource(int value)](#setFieldUpdateCultureSource-int-) | Указывает, какую культуру использовать для форматирования результата поля. |
| [setFieldUpdatingCallback(IFieldUpdatingCallback value)](#setFieldUpdatingCallback-com.aspose.words.IFieldUpdatingCallback-) |  Наборы[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) реализация |
| [setFileName(String value)](#setFileName-java.lang.String-) | Устанавливает имя файла документа. |
| [setLegacyNumberFormat(boolean value)](#setLegacyNumberFormat-boolean-) | Устанавливает значение, указывающее, включен ли устаревший (ранее, чем AW 13.10) числовой формат для полей. |
| [setPreProcessCulture(System.Globalization.CultureInfo value)](#setPreProcessCulture-com.aspose.words.net.System.Globalization.CultureInfo-) | Устанавливает культуру для предварительной обработки значений поля. |
| [setResultFormatter(IFieldResultFormatter value)](#setResultFormatter-com.aspose.words.IFieldResultFormatter-) | Позволяет управлять форматированием результата поля. |
| [setTemplateName(String value)](#setTemplateName-java.lang.String-) | Задает имя файла шаблона, используемого документом. |
| [setToaCategories(ToaCategories value)](#setToaCategories-com.aspose.words.ToaCategories-) | Задает таблицу категорий полномочий. |
| [setUseInvariantCultureNumberFormat(boolean value)](#setUseInvariantCultureNumberFormat-boolean-) | Задает значение, указывающее, что числовой формат анализируется с использованием инвариантного языка и региональных параметров или нет. |
| [setUserPromptRespondent(IFieldUserPromptRespondent value)](#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent-) | Настраивает респондента на подсказки пользователя во время обновления поля. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### getBarcodeGenerator() {#getBarcodeGenerator--}
```
public IBarcodeGenerator getBarcodeGenerator()
```


 Получает или задает пользовательский генератор штрих-кода. Пользовательский генератор штрих-кода должен реализовывать общедоступный интерфейс[IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator).

**Возвращает:**
[IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator) - Или установите пользовательский генератор штрих-кода.
### getBuiltInTemplatesPaths() {#getBuiltInTemplatesPaths--}
```
public String[] getBuiltInTemplatesPaths()
```


Получает пути к встроенным шаблонам MS Word.

 Это свойство используется[FieldAutoText](../../com.aspose.words/fieldautotext) а также[FieldGlossary](../../com.aspose.words/fieldglossary) полей, если указанная запись автотекста не найдена в[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) шаблон.

По умолчанию MS Word хранит встроенные шаблоны в c:\\Пользователи\\\\Данные приложения\\Роуминг\\Майкрософт\\Строительные блоки документа\\1033\\16\\Built-In Building Blocks.dotx и C:\\Пользователи\\\\Данные приложения\\Роуминг\\Майкрософт\\Шаблоны\Файлы \Normal.dotm.

**Возвращает:**
java.lang.String[] - Пути встроенных шаблонов MS Word.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getComparisonExpressionEvaluator() {#getComparisonExpressionEvaluator--}
```
public IComparisonExpressionEvaluator getComparisonExpressionEvaluator()
```


Получает средство оценки выражений сравнения полей.

**Возвращает:**
[IComparisonExpressionEvaluator](../../com.aspose.words/icomparisonexpressionevaluator) - Оценщик выражений сравнения полей.
### getCurrentUser() {#getCurrentUser--}
```
public UserInformation getCurrentUser()
```


Получает информацию о текущем пользователе.

**Возвращает:**
[UserInformation](../../com.aspose.words/userinformation) - Текущая информация о пользователе.
### getCustomTocStyleSeparator() {#getCustomTocStyleSeparator--}
```
public String getCustomTocStyleSeparator()
```


Получает разделитель пользовательского стиля для\ \t включить[FieldToc](../../com.aspose.words/fieldtoc) поле. По умолчанию пользовательские стили, определенные\ \t переключиться в[FieldToc](../../com.aspose.words/fieldtoc) поля разделены разделителем, взятым из текущей культуры. Это свойство переопределяет это поведение, указывая определяемый пользователем разделитель.

**Возвращает:**
 java.lang.String — разделитель пользовательского стиля для\ \t включить[FieldToc](../../com.aspose.words/fieldtoc) поле.
### getDefaultDocumentAuthor() {#getDefaultDocumentAuthor--}
```
public String getDefaultDocumentAuthor()
```


Получает имя автора документа по умолчанию. Если имя автора уже указано во встроенных свойствах документа, этот вариант не учитывается.

**Возвращает:**
java.lang.String — имя автора документа по умолчанию.
### getFieldDatabaseProvider() {#getFieldDatabaseProvider--}
```
public IFieldDatabaseProvider getFieldDatabaseProvider()
```


 Получает поставщика, который возвращает результат запроса для[FieldDatabase](../../com.aspose.words/fielddatabase) поле.

**Возвращает:**
[IFieldDatabaseProvider](../../com.aspose.words/ifielddatabaseprovider) - Провайдер, который возвращает результат запроса для[FieldDatabase](../../com.aspose.words/fielddatabase) поле.
### getFieldIndexFormat() {#getFieldIndexFormat--}
```
public int getFieldIndexFormat()
```


Получает[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) который представляет форматирование для[FieldIndex](../../com.aspose.words/fieldindex) поля в документе.

**Возвращает:**
 интервал - А[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) который представляет форматирование для[FieldIndex](../../com.aspose.words/fieldindex) поля в документе. Возвращаемое значение является одним из[FieldIndexFormat](../../com.aspose.words/fieldindexformat) константы.
### getFieldUpdateCultureProvider() {#getFieldUpdateCultureProvider--}
```
public IFieldUpdateCultureProvider getFieldUpdateCultureProvider()
```


Получает поставщика, возвращающего объект культуры для каждого конкретного поля.

 Провайдер запрашивается, когда значение[getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-) является**FieldUpdateCultureSource.FieldCode**.

Если поставщик присутствует, то возвращаемый им объект культуры используется для обновления поля. В противном случае используется системная культура.

**Возвращает:**
[IFieldUpdateCultureProvider](../../com.aspose.words/ifieldupdatecultureprovider) - Поставщик, возвращающий объект культуры для каждого конкретного поля.
### getFieldUpdateCultureSource() {#getFieldUpdateCultureSource--}
```
public int getFieldUpdateCultureSource()
```


Указывает, какую культуру использовать для форматирования результата поля.

По умолчанию используется культура текущего потока.

 Настройка влияет только на поля даты/времени с\\\Переключатель формата \@.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[FieldUpdateCultureSource](../../com.aspose.words/fieldupdateculturesource) константы.
### getFieldUpdatingCallback() {#getFieldUpdatingCallback--}
```
public IFieldUpdatingCallback getFieldUpdatingCallback()
```


 Получает[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) реализация

**Возвращает:**
[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) -\{[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) реализация
### getFileName() {#getFileName--}
```
public String getFileName()
```


Получает имя файла документа.

 Это свойство используется[FieldFileName](../../com.aspose.words/fieldfilename) поле с более высоким приоритетом, чем[Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--) имущество.

**Возвращает:**
java.lang.String — имя файла документа.
### getLegacyNumberFormat() {#getLegacyNumberFormat--}
```
public boolean getLegacyNumberFormat()
```


Получает значение, указывающее, включен ли устаревший (более ранний, чем AW 13.10) числовой формат для полей.

 Когда это свойство установлено в**true**, символ шаблона "\#" работает так же, как и в .net: заменяет знак решетки соответствующей цифрой, если она присутствует; в противном случае в строке результата символы не появляются.

 Когда это свойство установлено в**false**, символ шаблона "\ #" работает как MS Word: этот элемент формата указывает необходимые числовые позиции для отображения в результате. Если результат не содержит цифры в этом месте, MS Word отображает пробел. Например,\ { = 9 + 6\\\ #$\#\#\# \} отображает 15 долларов.

 Значение по умолчанию**false**.

**Возвращает:**
boolean — значение, указывающее, включен ли устаревший (до AW 13.10) числовой формат для полей или нет.
### getPreProcessCulture() {#getPreProcessCulture--}
```
public System.Globalization.CultureInfo getPreProcessCulture()
```


Получает культуру для предварительной обработки значений поля.

 В настоящее время это свойство влияет только на значение[FieldDocProperty](../../com.aspose.words/fielddocproperty) поле.

 Значение по умолчанию**null** . Когда это свойство установлено в**null** ,[FieldDocProperty](../../com.aspose.words/fielddocproperty) значение поля предварительно обрабатывается культурой, контролируемой[getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-) имущество.

**Возвращает:**
[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) - Культура для предварительной обработки значений полей.
### getResultFormatter() {#getResultFormatter--}
```
public IFieldResultFormatter getResultFormatter()
```


Позволяет управлять форматированием результата поля.

**Возвращает:**
[IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter) - соответствующий[IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter) ценность.
### getTemplateName() {#getTemplateName--}
```
public String getTemplateName()
```


Получает имя файла шаблона, используемого документом.

 Это свойство используется[FieldTemplate](../../com.aspose.words/fieldtemplate) поле, если[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) свойство пусто.

Если это свойство пусто, используется имя файла шаблона по умолчанию Normal.dotm.

**Возвращает:**
java.lang.String — имя файла шаблона, используемого документом.
### getToaCategories() {#getToaCategories--}
```
public ToaCategories getToaCategories()
```


Получает таблицу категорий полномочий.

**Возвращает:**
[ToaCategories](../../com.aspose.words/toacategories) Таблица категорий полномочий.
### getUseInvariantCultureNumberFormat() {#getUseInvariantCultureNumberFormat--}
```
public boolean getUseInvariantCultureNumberFormat()
```


Получает значение, указывающее, анализируется ли числовой формат с использованием инвариантного языка и региональных параметров.

 Когда это свойство установлено в**true**, числовой формат берется из инвариантного языка и региональных параметров.

 Когда это свойство установлено в**false**, числовой формат берется из культуры текущего потока.

 Значение по умолчанию**false**.

**Возвращает:**
boolean — значение, указывающее, что числовой формат анализируется с использованием инвариантной культуры или нет.
### getUserPromptRespondent() {#getUserPromptRespondent--}
```
public IFieldUserPromptRespondent getUserPromptRespondent()
```


Получает респондента на запросы пользователя во время обновления поля.

 Если значение этого свойства установлено в**null** , поля, которые требуют ответа пользователя при запросе (например,[FieldAsk](../../com.aspose.words/fieldask) или же[FieldFillIn](../../com.aspose.words/fieldfillin)) не обновляются.

 Значение по умолчанию**null**.

**Возвращает:**
[IFieldUserPromptRespondent](../../com.aspose.words/ifielduserpromptrespondent) - Ответчик на запросы пользователя во время обновления поля.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isBidiTextSupportedOnUpdate() {#isBidiTextSupportedOnUpdate--}
```
public boolean isBidiTextSupportedOnUpdate()
```


Получает значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля.

 Когда это свойство установлено в**true**, выполняются дополнительные шаги для создания результата поля, совместимого с написанием справа налево (т. е. арабского или иврита), во время его обновления.

 Когда это свойство установлено в**false** и используется язык справа налево, корректность результата поля после его обновления не гарантируется.

 Значение по умолчанию**false**.

**Возвращает:**
boolean — значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля или нет.
### isBidiTextSupportedOnUpdate(boolean value) {#isBidiTextSupportedOnUpdate-boolean-}
```
public void isBidiTextSupportedOnUpdate(boolean value)
```


Задает значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля.

 Когда это свойство установлено в**true**, выполняются дополнительные шаги для создания результата поля, совместимого с написанием справа налево (т. е. арабского или иврита), во время его обновления.

 Когда это свойство установлено в**false** и используется язык справа налево, корректность результата поля после его обновления не гарантируется.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля. |

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


 Получает или задает пользовательский генератор штрих-кода. Пользовательский генератор штрих-кода должен реализовывать общедоступный интерфейс[IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IBarcodeGenerator](../../com.aspose.words/ibarcodegenerator) | Или установите собственный генератор штрих-кода. |

### setBuiltInTemplatesPaths(String[] value) {#setBuiltInTemplatesPaths-java.lang.String---}
```
public void setBuiltInTemplatesPaths(String[] value)
```


Задает пути к встроенным шаблонам MS Word.

 Это свойство используется[FieldAutoText](../../com.aspose.words/fieldautotext) а также[FieldGlossary](../../com.aspose.words/fieldglossary) полей, если указанная запись автотекста не найдена в[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) шаблон.

По умолчанию MS Word хранит встроенные шаблоны в c:\\Пользователи\\\\Данные приложения\\Роуминг\\Майкрософт\\Строительные блоки документа\\1033\\16\\Built-In Building Blocks.dotx и C:\\Пользователи\\\\Данные приложения\\Роуминг\\Майкрософт\\Шаблоны\Файлы \Normal.dotm.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String[] | Пути встроенных шаблонов MS Word. |

### setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value) {#setComparisonExpressionEvaluator-com.aspose.words.IComparisonExpressionEvaluator-}
```
public void setComparisonExpressionEvaluator(IComparisonExpressionEvaluator value)
```


Устанавливает оценщик выражений сравнения полей.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IComparisonExpressionEvaluator](../../com.aspose.words/icomparisonexpressionevaluator) | Оценщик выражений сравнения полей. |

### setCurrentUser(UserInformation value) {#setCurrentUser-com.aspose.words.UserInformation-}
```
public void setCurrentUser(UserInformation value)
```


Устанавливает текущую информацию о пользователе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [UserInformation](../../com.aspose.words/userinformation) | Информация о текущем пользователе. |

### setCustomTocStyleSeparator(String value) {#setCustomTocStyleSeparator-java.lang.String-}
```
public void setCustomTocStyleSeparator(String value)
```


 Устанавливает разделитель пользовательского стиля для\ \t включить[FieldToc](../../com.aspose.words/fieldtoc) поле. По умолчанию пользовательские стили, определенные\ \t переключиться в[FieldToc](../../com.aspose.words/fieldtoc) поля разделены разделителем, взятым из текущей культуры. Это свойство переопределяет это поведение, указывая определяемый пользователем разделитель.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String |  Пользовательский разделитель стилей для\ \t включить[FieldToc](../../com.aspose.words/fieldtoc) поле. |

### setDefaultDocumentAuthor(String value) {#setDefaultDocumentAuthor-java.lang.String-}
```
public void setDefaultDocumentAuthor(String value)
```


Устанавливает имя автора документа по умолчанию. Если имя автора уже указано во встроенных свойствах документа, этот вариант не учитывается.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя автора документа по умолчанию. |

### setFieldDatabaseProvider(IFieldDatabaseProvider value) {#setFieldDatabaseProvider-com.aspose.words.IFieldDatabaseProvider-}
```
public void setFieldDatabaseProvider(IFieldDatabaseProvider value)
```


 Задает поставщика, который возвращает результат запроса для[FieldDatabase](../../com.aspose.words/fielddatabase) поле.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IFieldDatabaseProvider](../../com.aspose.words/ifielddatabaseprovider) |  Провайдер, который возвращает результат запроса для[FieldDatabase](../../com.aspose.words/fielddatabase) поле. |

### setFieldIndexFormat(int value) {#setFieldIndexFormat-int-}
```
public void setFieldIndexFormat(int value)
```


 Устанавливает[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) который представляет форматирование для[FieldIndex](../../com.aspose.words/fieldindex) поля в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  А[getFieldIndexFormat()](../../com.aspose.words/fieldoptions\#getFieldIndexFormat--) / [setFieldIndexFormat(int)](../../com.aspose.words/fieldoptions\#setFieldIndexFormat-int-) который представляет форматирование для[FieldIndex](../../com.aspose.words/fieldindex) поля в документе. Значение должно быть одним из[FieldIndexFormat](../../com.aspose.words/fieldindexformat) константы. |

### setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value) {#setFieldUpdateCultureProvider-com.aspose.words.IFieldUpdateCultureProvider-}
```
public void setFieldUpdateCultureProvider(IFieldUpdateCultureProvider value)
```


Задает поставщика, который возвращает объект культуры для каждого конкретного поля.

 Провайдер запрашивается, когда значение[getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-) является**FieldUpdateCultureSource.FieldCode**.

Если поставщик присутствует, то возвращаемый им объект культуры используется для обновления поля. В противном случае используется системная культура.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IFieldUpdateCultureProvider](../../com.aspose.words/ifieldupdatecultureprovider) | Поставщик, возвращающий объект культуры для каждого конкретного поля. |

### setFieldUpdateCultureSource(int value) {#setFieldUpdateCultureSource-int-}
```
public void setFieldUpdateCultureSource(int value)
```


Указывает, какую культуру использовать для форматирования результата поля.

По умолчанию используется культура текущего потока.

 Настройка влияет только на поля даты/времени с\\\Переключатель формата \@.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[FieldUpdateCultureSource](../../com.aspose.words/fieldupdateculturesource) константы. |

### setFieldUpdatingCallback(IFieldUpdatingCallback value) {#setFieldUpdatingCallback-com.aspose.words.IFieldUpdatingCallback-}
```
public void setFieldUpdatingCallback(IFieldUpdatingCallback value)
```


 Наборы[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) реализация

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) | \{[IFieldUpdatingCallback](../../com.aspose.words/ifieldupdatingcallback) реализация |

### setFileName(String value) {#setFileName-java.lang.String-}
```
public void setFileName(String value)
```


Устанавливает имя файла документа.

 Это свойство используется[FieldFileName](../../com.aspose.words/fieldfilename) поле с более высоким приоритетом, чем[Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--) имущество.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя файла документа. |

### setLegacyNumberFormat(boolean value) {#setLegacyNumberFormat-boolean-}
```
public void setLegacyNumberFormat(boolean value)
```


Устанавливает значение, указывающее, включен ли устаревший (ранее, чем AW 13.10) числовой формат для полей.

 Когда это свойство установлено в**true**, символ шаблона "\#" работает так же, как и в .net: заменяет знак решетки соответствующей цифрой, если она присутствует; в противном случае в строке результата символы не появляются.

 Когда это свойство установлено в**false**, символ шаблона "\ #" работает как MS Word: этот элемент формата указывает необходимые числовые позиции для отображения в результате. Если результат не содержит цифры в этом месте, MS Word отображает пробел. Например,\ { = 9 + 6\\\ #$\#\#\# \} отображает 15 долларов.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, включен ли устаревший (ранее, чем AW 13.10) числовой формат для полей. |

### setPreProcessCulture(System.Globalization.CultureInfo value) {#setPreProcessCulture-com.aspose.words.net.System.Globalization.CultureInfo-}
```
public void setPreProcessCulture(System.Globalization.CultureInfo value)
```


Устанавливает культуру для предварительной обработки значений поля.

 В настоящее время это свойство влияет только на значение[FieldDocProperty](../../com.aspose.words/fielddocproperty) поле.

 Значение по умолчанию**null** . Когда это свойство установлено в**null** ,[FieldDocProperty](../../com.aspose.words/fielddocproperty) значение поля предварительно обрабатывается культурой, контролируемой[getFieldUpdateCultureSource()](../../com.aspose.words/fieldoptions\#getFieldUpdateCultureSource--) / [setFieldUpdateCultureSource(int)](../../com.aspose.words/fieldoptions\#setFieldUpdateCultureSource-int-) имущество.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) | Культура для предварительной обработки значений поля. |

### setResultFormatter(IFieldResultFormatter value) {#setResultFormatter-com.aspose.words.IFieldResultFormatter-}
```
public void setResultFormatter(IFieldResultFormatter value)
```


Позволяет управлять форматированием результата поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter) |  Соответствующий[IFieldResultFormatter](../../com.aspose.words/ifieldresultformatter) ценность. |

### setTemplateName(String value) {#setTemplateName-java.lang.String-}
```
public void setTemplateName(String value)
```


Задает имя файла шаблона, используемого документом.

 Это свойство используется[FieldTemplate](../../com.aspose.words/fieldtemplate) поле, если[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) свойство пусто.

Если это свойство пусто, используется имя файла шаблона по умолчанию Normal.dotm.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя файла шаблона, используемого документом. |

### setToaCategories(ToaCategories value) {#setToaCategories-com.aspose.words.ToaCategories-}
```
public void setToaCategories(ToaCategories value)
```


Задает таблицу категорий полномочий.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [ToaCategories](../../com.aspose.words/toacategories) | Таблица категорий полномочий. |

### setUseInvariantCultureNumberFormat(boolean value) {#setUseInvariantCultureNumberFormat-boolean-}
```
public void setUseInvariantCultureNumberFormat(boolean value)
```


Задает значение, указывающее, что числовой формат анализируется с использованием инвариантного языка и региональных параметров или нет.

 Когда это свойство установлено в**true**, числовой формат берется из инвариантного языка и региональных параметров.

 Когда это свойство установлено в**false**, числовой формат берется из культуры текущего потока.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, что числовой формат анализируется с использованием инвариантного языка и региональных параметров или нет. |

### setUserPromptRespondent(IFieldUserPromptRespondent value) {#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent-}
```
public void setUserPromptRespondent(IFieldUserPromptRespondent value)
```


Настраивает респондента на подсказки пользователя во время обновления поля.

 Если значение этого свойства установлено в**null** , поля, которые требуют ответа пользователя при запросе (например,[FieldAsk](../../com.aspose.words/fieldask) или же[FieldFillIn](../../com.aspose.words/fieldfillin)) не обновляются.

 Значение по умолчанию**null**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IFieldUserPromptRespondent](../../com.aspose.words/ifielduserpromptrespondent) | Ответчик на запросы пользователя во время обновления поля. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
