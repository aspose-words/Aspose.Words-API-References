---
title: FindReplaceOptions
second_title: Справочник по API Aspose.Words для Java
description: Задает параметры операций поиска/замены.
type: docs
weight: 270
url: /ru/java/com.aspose.words/findreplaceoptions/
---

**Наследование:**
java.lang.Object
```
public class FindReplaceOptions
```

Задает параметры операций поиска/замены.

 Чтобы узнать больше, посетите**Find and Replace** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [FindReplaceOptions()](#FindReplaceOptions--) | Инициализирует новый экземпляр этого класса. |
| [FindReplaceOptions(int direction)](#FindReplaceOptions-int-) | Инициализирует новый экземпляр этого класса. |
| [FindReplaceOptions(IReplacingCallback replacingCallback)](#FindReplaceOptions-com.aspose.words.IReplacingCallback-) | Инициализирует новый экземпляр этого класса. |
| [FindReplaceOptions(int direction, IReplacingCallback replacingCallback)](#FindReplaceOptions-int-com.aspose.words.IReplacingCallback-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getApplyFont()](#getApplyFont--) | Форматирование текста применяется к новому содержимому. |
| [getApplyParagraphFormat()](#getApplyParagraphFormat--) | Форматирование абзаца применяется к новому содержимому. |
| [getClass()](#getClass--) |  |
| [getDirection()](#getDirection--) | Выбирает направление для замены. |
| [getFindWholeWordsOnly()](#getFindWholeWordsOnly--) | True указывает, что oldValue должно быть отдельным словом. |
| [getIgnoreDeleted()](#getIgnoreDeleted--) | Получает логическое значение, указывающее, следует ли игнорировать текст внутри удаления ревизий. |
| [getIgnoreFieldCodes()](#getIgnoreFieldCodes--) | Получает логическое значение, указывающее, следует ли игнорировать текст внутри кодов полей. |
| [getIgnoreFields()](#getIgnoreFields--) | Получает логическое значение, указывающее, следует ли игнорировать текст внутри полей. |
| [getIgnoreFootnotes()](#getIgnoreFootnotes--) | Получает логическое значение, указывающее, следует ли игнорировать сноски. |
| [getIgnoreInserted()](#getIgnoreInserted--) | Получает логическое значение, указывающее, следует ли игнорировать текст внутри ревизий вставки. |
| [getIgnoreStructuredDocumentTags()](#getIgnoreStructuredDocumentTags--) |  Получает логическое значение, указывающее либо игнорировать содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |
| [getLegacyMode()](#getLegacyMode--) | Получает логическое значение, указывающее, что используется старый алгоритм поиска/замены. |
| [getMatchCase()](#getMatchCase--) | True указывает на сравнение с учетом регистра, false указывает на сравнение без учета регистра. |
| [getReplacingCallback()](#getReplacingCallback--) | Пользовательский метод, который вызывается перед каждой заменой. |
| [getSmartParagraphBreakReplacement()](#getSmartParagraphBreakReplacement--) | Получает или задает логическое значение, указывающее, разрешено ли заменять разрыв абзаца, если нет следующего одноуровневого абзаца. |
| [getUseLegacyOrder()](#getUseLegacyOrder--) | True указывает, что текстовый поиск выполняется последовательно сверху вниз с учетом текстовых полей. |
| [getUseSubstitutions()](#getUseSubstitutions--) | Получает логическое значение, указывающее, следует ли распознавать и использовать замены в шаблонах замены. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDirection(int value)](#setDirection-int-) | Выбирает направление для замены. |
| [setFindWholeWordsOnly(boolean value)](#setFindWholeWordsOnly-boolean-) | True указывает, что oldValue должно быть отдельным словом. |
| [setIgnoreDeleted(boolean value)](#setIgnoreDeleted-boolean-) | Устанавливает логическое значение, указывающее либо игнорировать текст внутри удаляемых ревизий. |
| [setIgnoreFieldCodes(boolean value)](#setIgnoreFieldCodes-boolean-) | Задает логическое значение, указывающее либо игнорировать текст внутри кодов полей. |
| [setIgnoreFields(boolean value)](#setIgnoreFields-boolean-) | Задает логическое значение, указывающее либо игнорировать текст внутри полей. |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean-) | Устанавливает логическое значение, указывающее либо игнорировать сноски. |
| [setIgnoreInserted(boolean value)](#setIgnoreInserted-boolean-) | Устанавливает логическое значение, указывающее либо игнорировать текст внутри ревизий вставки. |
| [setIgnoreStructuredDocumentTags(boolean value)](#setIgnoreStructuredDocumentTags-boolean-) |  Устанавливает логическое значение, указывающее либо игнорировать содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |
| [setLegacyMode(boolean value)](#setLegacyMode-boolean-) | Задает логическое значение, указывающее, что используется старый алгоритм поиска/замены. |
| [setMatchCase(boolean value)](#setMatchCase-boolean-) | True указывает на сравнение с учетом регистра, false указывает на сравнение без учета регистра. |
| [setReplacingCallback(IReplacingCallback value)](#setReplacingCallback-com.aspose.words.IReplacingCallback-) | Пользовательский метод, который вызывается перед каждой заменой. |
| [setSmartParagraphBreakReplacement(boolean value)](#setSmartParagraphBreakReplacement-boolean-) | Получает или задает логическое значение, указывающее, разрешено ли заменять разрыв абзаца, если нет следующего одноуровневого абзаца. |
| [setUseLegacyOrder(boolean value)](#setUseLegacyOrder-boolean-) | True указывает, что текстовый поиск выполняется последовательно сверху вниз с учетом текстовых полей. |
| [setUseSubstitutions(boolean value)](#setUseSubstitutions-boolean-) | Задает логическое значение, указывающее, следует ли распознавать и использовать замены в шаблонах замены. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FindReplaceOptions() {#FindReplaceOptions--}
```
public FindReplaceOptions()
```


Инициализирует новый экземпляр этого класса.

### FindReplaceOptions(int direction) {#FindReplaceOptions-int-}
```
public FindReplaceOptions(int direction)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| direction | int |  |

### FindReplaceOptions(IReplacingCallback replacingCallback) {#FindReplaceOptions-com.aspose.words.IReplacingCallback-}
```
public FindReplaceOptions(IReplacingCallback replacingCallback)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) |  |

### FindReplaceOptions(int direction, IReplacingCallback replacingCallback) {#FindReplaceOptions-int-com.aspose.words.IReplacingCallback-}
```
public FindReplaceOptions(int direction, IReplacingCallback replacingCallback)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| direction | int |  |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) |  |

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
### getApplyFont() {#getApplyFont--}
```
public Font getApplyFont()
```


Форматирование текста применяется к новому содержимому.

**Возвращает:**
[Font](../../com.aspose.words/font) - соответствующий[Font](../../com.aspose.words/font) ценность.
### getApplyParagraphFormat() {#getApplyParagraphFormat--}
```
public ParagraphFormat getApplyParagraphFormat()
```


Форматирование абзаца применяется к новому содержимому.

**Возвращает:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - соответствующий[ParagraphFormat](../../com.aspose.words/paragraphformat) ценность.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDirection() {#getDirection--}
```
public int getDirection()
```


 Выбирает направление для замены. Значение по умолчанию[FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection\#FORWARD).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[FindReplaceDirection](../../com.aspose.words/findreplacedirection) константы.
### getFindWholeWordsOnly() {#getFindWholeWordsOnly--}
```
public boolean getFindWholeWordsOnly()
```


True указывает, что oldValue должно быть отдельным словом.

**Возвращает:**
boolean - соответствующее логическое значение.
### getIgnoreDeleted() {#getIgnoreDeleted--}
```
public boolean getIgnoreDeleted()
```


Получает логическое значение, указывающее, следует ли игнорировать текст внутри удаления ревизий. Значение по умолчанию неверно .

**Возвращает:**
boolean — логическое значение, указывающее либо игнорировать текст внутри удаляемых ревизий.
### getIgnoreFieldCodes() {#getIgnoreFieldCodes--}
```
public boolean getIgnoreFieldCodes()
```


Получает логическое значение, указывающее, следует ли игнорировать текст внутри кодов полей. Значение по умолчанию неверно .

 Этот параметр влияет только на коды полей (он не игнорирует узлы между[NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype\#FIELD-SEPARATOR) а также[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)).

 Чтобы игнорировать все поле, используйте соответствующую опцию[getIgnoreFields()](../../com.aspose.words/findreplaceoptions\#getIgnoreFields--) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFields-boolean-).

**Возвращает:**
boolean — логическое значение, указывающее, следует ли игнорировать текст внутри кодов полей.
### getIgnoreFields() {#getIgnoreFields--}
```
public boolean getIgnoreFields()
```


Получает логическое значение, указывающее, следует ли игнорировать текст внутри полей. Значение по умолчанию неверно .

 Этот параметр влияет на все поле (все узлы между[NodeType.FIELD\_START](../../com.aspose.words/nodetype\#FIELD-START) а также[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)).

 Чтобы игнорировать только коды полей, используйте соответствующую опцию[getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions\#getIgnoreFieldCodes--) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFieldCodes-boolean-).

**Возвращает:**
boolean — логическое значение, указывающее, следует ли игнорировать текст внутри полей.
### getIgnoreFootnotes() {#getIgnoreFootnotes--}
```
public boolean getIgnoreFootnotes()
```


Получает логическое значение, указывающее, следует ли игнорировать сноски. Значение по умолчанию неверно .

**Возвращает:**
boolean — логическое значение, указывающее, следует ли игнорировать сноски.
### getIgnoreInserted() {#getIgnoreInserted--}
```
public boolean getIgnoreInserted()
```


Получает логическое значение, указывающее, следует ли игнорировать текст внутри ревизий вставки. Значение по умолчанию неверно .

**Возвращает:**
boolean — логическое значение, указывающее, следует ли игнорировать текст внутри ревизий вставки.
### getIgnoreStructuredDocumentTags() {#getIgnoreStructuredDocumentTags--}
```
public boolean getIgnoreStructuredDocumentTags()
```


 Получает логическое значение, указывающее либо игнорировать содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)Значение по умолчанию неверно .

 Когда для этой опции установлено значение true , содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) будет рассматриваться как простой текст.

 В противном случае,[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) будет обрабатываться как отдельная история, а заменяющий шаблон будет искаться отдельно для каждого[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) , так что если образец пересекает[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag), то для такого шаблона замена производиться не будет.

**Возвращает:**
 boolean — логическое значение, указывающее либо на игнорирование содержимого[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).
### getLegacyMode() {#getLegacyMode--}
```
public boolean getLegacyMode()
```


Получает логическое значение, указывающее, что используется старый алгоритм поиска/замены. Используйте этот флаг, если вам нужно точно такое же поведение, как и до введения расширенной функции поиска/замены. Обратите внимание, что старый алгоритм не поддерживает расширенные функции, такие как замена разрывами, применение форматирования и т. д.

**Возвращает:**
boolean — логическое значение, указывающее, что используется старый алгоритм поиска/замены.
### getMatchCase() {#getMatchCase--}
```
public boolean getMatchCase()
```


True указывает на сравнение с учетом регистра, false указывает на сравнение без учета регистра.

**Возвращает:**
boolean - соответствующее логическое значение.
### getReplacingCallback() {#getReplacingCallback--}
```
public IReplacingCallback getReplacingCallback()
```


Пользовательский метод, который вызывается перед каждой заменой.

**Возвращает:**
[IReplacingCallback](../../com.aspose.words/ireplacingcallback) - соответствующий[IReplacingCallback](../../com.aspose.words/ireplacingcallback) ценность.
### getSmartParagraphBreakReplacement() {#getSmartParagraphBreakReplacement--}
```
public boolean getSmartParagraphBreakReplacement()
```


Получает или задает логическое значение, указывающее, разрешено ли заменять разрыв абзаца, если нет следующего одноуровневого абзаца.

Значение по умолчанию неверно .

Эта опция позволяет заменить разрыв абзаца, когда нет следующего одноуровневого абзаца, в который можно переместить все дочерние узлы, найдя любой (не обязательно одноуровневый) следующий абзац после заменяемого абзаца.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUseLegacyOrder() {#getUseLegacyOrder--}
```
public boolean getUseLegacyOrder()
```


True указывает, что текстовый поиск выполняется последовательно сверху вниз с учетом текстовых полей. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getUseSubstitutions() {#getUseSubstitutions--}
```
public boolean getUseSubstitutions()
```


Получает логическое значение, указывающее, следует ли распознавать и использовать замены в шаблонах замены. Значение по умолчанию неверно . Дополнительные сведения об элементах замены см. по адресу: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

**Возвращает:**
boolean — логическое значение, указывающее, следует ли распознавать и использовать замены в шаблонах замены.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setDirection(int value) {#setDirection-int-}
```
public void setDirection(int value)
```


 Выбирает направление для замены. Значение по умолчанию[FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection\#FORWARD).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[FindReplaceDirection](../../com.aspose.words/findreplacedirection) константы. |

### setFindWholeWordsOnly(boolean value) {#setFindWholeWordsOnly-boolean-}
```
public void setFindWholeWordsOnly(boolean value)
```


True указывает, что oldValue должно быть отдельным словом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setIgnoreDeleted(boolean value) {#setIgnoreDeleted-boolean-}
```
public void setIgnoreDeleted(boolean value)
```


Устанавливает логическое значение, указывающее либо игнорировать текст внутри удаляемых ревизий. Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, следует ли игнорировать текст внутри ревизий удаления. |

### setIgnoreFieldCodes(boolean value) {#setIgnoreFieldCodes-boolean-}
```
public void setIgnoreFieldCodes(boolean value)
```


Задает логическое значение, указывающее либо игнорировать текст внутри кодов полей. Значение по умолчанию неверно .

 Этот параметр влияет только на коды полей (он не игнорирует узлы между[NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype\#FIELD-SEPARATOR) а также[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)).

 Чтобы игнорировать все поле, используйте соответствующую опцию[getIgnoreFields()](../../com.aspose.words/findreplaceoptions\#getIgnoreFields--) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFields-boolean-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее либо игнорировать текст внутри кодов полей. |

### setIgnoreFields(boolean value) {#setIgnoreFields-boolean-}
```
public void setIgnoreFields(boolean value)
```


Задает логическое значение, указывающее либо игнорировать текст внутри полей. Значение по умолчанию неверно .

 Этот параметр влияет на все поле (все узлы между[NodeType.FIELD\_START](../../com.aspose.words/nodetype\#FIELD-START) а также[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)).

 Чтобы игнорировать только коды полей, используйте соответствующую опцию[getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions\#getIgnoreFieldCodes--) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFieldCodes-boolean-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее либо игнорировать текст внутри полей. |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean-}
```
public void setIgnoreFootnotes(boolean value)
```


Устанавливает логическое значение, указывающее либо игнорировать сноски. Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, следует ли игнорировать сноски. |

### setIgnoreInserted(boolean value) {#setIgnoreInserted-boolean-}
```
public void setIgnoreInserted(boolean value)
```


Устанавливает логическое значение, указывающее либо игнорировать текст внутри ревизий вставки. Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее либо игнорировать текст внутри ревизий вставки. |

### setIgnoreStructuredDocumentTags(boolean value) {#setIgnoreStructuredDocumentTags-boolean-}
```
public void setIgnoreStructuredDocumentTags(boolean value)
```


 Устанавливает логическое значение, указывающее либо игнорировать содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)Значение по умолчанию неверно .

 Когда для этой опции установлено значение true , содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) будет рассматриваться как простой текст.

 В противном случае,[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) будет обрабатываться как отдельная история, а заменяющий шаблон будет искаться отдельно для каждого[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) , так что если образец пересекает[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag), то для такого шаблона замена производиться не будет.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Логическое значение, указывающее либо на игнорирование содержимого[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |

### setLegacyMode(boolean value) {#setLegacyMode-boolean-}
```
public void setLegacyMode(boolean value)
```


Задает логическое значение, указывающее, что используется старый алгоритм поиска/замены. Используйте этот флаг, если вам нужно точно такое же поведение, как и до введения расширенной функции поиска/замены. Обратите внимание, что старый алгоритм не поддерживает расширенные функции, такие как замена разрывами, применение форматирования и т. д.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, что используется старый алгоритм поиска/замены. |

### setMatchCase(boolean value) {#setMatchCase-boolean-}
```
public void setMatchCase(boolean value)
```


True указывает на сравнение с учетом регистра, false указывает на сравнение без учета регистра.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setReplacingCallback(IReplacingCallback value) {#setReplacingCallback-com.aspose.words.IReplacingCallback-}
```
public void setReplacingCallback(IReplacingCallback value)
```


Пользовательский метод, который вызывается перед каждой заменой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) |  Соответствующий[IReplacingCallback](../../com.aspose.words/ireplacingcallback) ценность. |

### setSmartParagraphBreakReplacement(boolean value) {#setSmartParagraphBreakReplacement-boolean-}
```
public void setSmartParagraphBreakReplacement(boolean value)
```


Получает или задает логическое значение, указывающее, разрешено ли заменять разрыв абзаца, если нет следующего одноуровневого абзаца.

Значение по умолчанию неверно .

Эта опция позволяет заменить разрыв абзаца, когда нет следующего одноуровневого абзаца, в который можно переместить все дочерние узлы, найдя любой (не обязательно одноуровневый) следующий абзац после заменяемого абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUseLegacyOrder(boolean value) {#setUseLegacyOrder-boolean-}
```
public void setUseLegacyOrder(boolean value)
```


True указывает, что текстовый поиск выполняется последовательно сверху вниз с учетом текстовых полей. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setUseSubstitutions(boolean value) {#setUseSubstitutions-boolean-}
```
public void setUseSubstitutions(boolean value)
```


Задает логическое значение, указывающее, следует ли распознавать и использовать замены в шаблонах замены. Значение по умолчанию неверно . Дополнительные сведения об элементах замены см. по адресу: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, следует ли распознавать и использовать замены в шаблонах замены. |

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
