---
title: LayoutOptions
second_title: Справочник по API Aspose.Words для Java
description: Содержит параметры, позволяющие управлять процессом верстки документа.
type: docs
weight: 362
url: /ru/java/com.aspose.words/layoutoptions/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class LayoutOptions implements Cloneable
```

Содержит параметры, позволяющие управлять процессом верстки документа.

 Чтобы узнать больше, посетите**Converting to Fixed-page Format** документальная статья.

Вы не создаете экземпляры этого класса напрямую. Использовать[Document.getLayoutOptions()](../../com.aspose.words/document\#getLayoutOptions--) свойство для доступа к параметрам макета для этого документа.

 Обратите внимание, что после изменения любого из параметров, присутствующих в этом классе,[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) метод должен быть вызван для того, чтобы измененные параметры были применены к макету.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCallback()](#getCallback--) |  Получает[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) реализация, используемая моделью макета страницы. |
| [getClass()](#getClass--) |  |
| [getCommentDisplayMode()](#getCommentDisplayMode--) | Получает способ отображения комментариев. |
| [getContinuousSectionPageNumberingRestart()](#getContinuousSectionPageNumberingRestart--) | Получает режим поведения для вычисления номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц. |
| [getIgnorePrinterMetrics()](#getIgnorePrinterMetrics--) | Получает указание на то, игнорируется ли параметр совместимости «Использовать метрики принтера для компоновки документа». |
| [getRevisionOptions()](#getRevisionOptions--) | Получает параметры редакции. |
| [getShowHiddenText()](#getShowHiddenText--) | Получает указание на то, отображается ли скрытый текст в документе. |
| [getShowParagraphMarks()](#getShowParagraphMarks--) | Получает индикацию того, отображаются ли метки абзаца. |
| [getTextShaperFactory()](#getTextShaperFactory--) |  Получает[ITextShaperFactory](../../com.aspose.words/itextshaperfactory) реализация, используемая для функций рендеринга Advanced Typography. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCallback(IPageLayoutCallback value)](#setCallback-com.aspose.words.IPageLayoutCallback-) |  Наборы[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) реализация, используемая моделью макета страницы. |
| [setCommentDisplayMode(int value)](#setCommentDisplayMode-int-) | Устанавливает способ отображения комментариев. |
| [setContinuousSectionPageNumberingRestart(int value)](#setContinuousSectionPageNumberingRestart-int-) | Устанавливает режим поведения для вычисления номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц. |
| [setIgnorePrinterMetrics(boolean value)](#setIgnorePrinterMetrics-boolean-) | Устанавливает индикацию того, игнорируется ли параметр совместимости «Использовать метрики принтера для макета документа». |
| [setShowHiddenText(boolean value)](#setShowHiddenText-boolean-) | Устанавливает индикацию того, отображается ли скрытый текст в документе. |
| [setShowParagraphMarks(boolean value)](#setShowParagraphMarks-boolean-) | Устанавливает индикацию того, отображаются ли метки абзаца. |
| [setTextShaperFactory(ITextShaperFactory value)](#setTextShaperFactory-com.aspose.words.ITextShaperFactory-) |  Наборы[ITextShaperFactory](../../com.aspose.words/itextshaperfactory) реализация, используемая для функций рендеринга Advanced Typography. |
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
### getCallback() {#getCallback--}
```
public IPageLayoutCallback getCallback()
```


 Получает[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) реализация, используемая моделью макета страницы.

**Возвращает:**
[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) -\{[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) реализация, используемая моделью макета страницы.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCommentDisplayMode() {#getCommentDisplayMode--}
```
public int getCommentDisplayMode()
```


 Получает способ отображения комментариев. Значение по умолчанию[CommentDisplayMode.SHOW\_IN\_BALLOONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-BALLOONS) . Обратите внимание, что исправления не отображаются во всплывающих подсказках для[CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**Возвращает:**
 int — способ отображения комментариев. Возвращаемое значение является одним из[CommentDisplayMode](../../com.aspose.words/commentdisplaymode) константы.
### getContinuousSectionPageNumberingRestart() {#getContinuousSectionPageNumberingRestart--}
```
public int getContinuousSectionPageNumberingRestart()
```


Получает режим поведения для вычисления номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц. Значение по умолчанию[ContinuousSectionRestart.ALWAYS](../../com.aspose.words/continuoussectionrestart\#ALWAYS) . Это соответствует поведению MS Word 2019, который был последней версией на момент введения этой опции. С помощью этой опции доступна старая логика нумерации страниц, продемонстрированная в MS Word 2016. Пожалуйста[ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart) для описания поведения.

**Возвращает:**
 int — режим поведения для вычисления номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц. Возвращаемое значение является одним из[ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart) константы.
### getIgnorePrinterMetrics() {#getIgnorePrinterMetrics--}
```
public boolean getIgnorePrinterMetrics()
```


Получает указание на то, игнорируется ли параметр совместимости «Использовать метрики принтера для компоновки документа». Значение по умолчанию — Истина.

**Возвращает:**
boolean — указывает, игнорируется ли параметр совместимости «Использовать метрики принтера для компоновки документа».
### getRevisionOptions() {#getRevisionOptions--}
```
public RevisionOptions getRevisionOptions()
```


Получает параметры редакции.

**Возвращает:**
[RevisionOptions](../../com.aspose.words/revisionoptions) - Варианты ревизии.
### getShowHiddenText() {#getShowHiddenText--}
```
public boolean getShowHiddenText()
```


Получает указание на то, отображается ли скрытый текст в документе. По умолчанию — Ложь. Это свойство влияет на весь скрытый контент, а не только на текст.

**Возвращает:**
boolean — указывает, отображается ли скрытый текст в документе.
### getShowParagraphMarks() {#getShowParagraphMarks--}
```
public boolean getShowParagraphMarks()
```


Получает индикацию того, отображаются ли метки абзаца. По умолчанию — Ложь.

**Возвращает:**
boolean — указывает, отображаются ли метки абзаца.
### getTextShaperFactory() {#getTextShaperFactory--}
```
public ITextShaperFactory getTextShaperFactory()
```


 Получает[ITextShaperFactory](../../com.aspose.words/itextshaperfactory) реализация, используемая для функций рендеринга Advanced Typography.

**Возвращает:**
[ITextShaperFactory](../../com.aspose.words/itextshaperfactory) -\{[ITextShaperFactory](../../com.aspose.words/itextshaperfactory) реализация, используемая для функций рендеринга Advanced Typography.
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




### setCallback(IPageLayoutCallback value) {#setCallback-com.aspose.words.IPageLayoutCallback-}
```
public void setCallback(IPageLayoutCallback value)
```


 Наборы[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) реализация, используемая моделью макета страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) | \{[IPageLayoutCallback](../../com.aspose.words/ipagelayoutcallback) реализация, используемая моделью макета страницы. |

### setCommentDisplayMode(int value) {#setCommentDisplayMode-int-}
```
public void setCommentDisplayMode(int value)
```


 Устанавливает способ отображения комментариев. Значение по умолчанию[CommentDisplayMode.SHOW\_IN\_BALLOONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-BALLOONS) . Обратите внимание, что исправления не отображаются во всплывающих подсказках для[CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Способ отображения комментариев. Значение должно быть одним из[CommentDisplayMode](../../com.aspose.words/commentdisplaymode) константы. |

### setContinuousSectionPageNumberingRestart(int value) {#setContinuousSectionPageNumberingRestart-int-}
```
public void setContinuousSectionPageNumberingRestart(int value)
```


 Устанавливает режим поведения для вычисления номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц. Значение по умолчанию[ContinuousSectionRestart.ALWAYS](../../com.aspose.words/continuoussectionrestart\#ALWAYS) . Это соответствует поведению MS Word 2019, который был последней версией на момент введения этой опции. С помощью этой опции доступна старая логика нумерации страниц, продемонстрированная в MS Word 2016. Пожалуйста[ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart) для описания поведения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Режим поведения для вычисления номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц. Значение должно быть одним из[ContinuousSectionRestart](../../com.aspose.words/continuoussectionrestart) константы. |

### setIgnorePrinterMetrics(boolean value) {#setIgnorePrinterMetrics-boolean-}
```
public void setIgnorePrinterMetrics(boolean value)
```


Устанавливает индикацию того, игнорируется ли параметр совместимости «Использовать метрики принтера для макета документа». Значение по умолчанию — Истина.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Указание на то, игнорируется ли параметр совместимости «Использовать метрики принтера для макета документа». |

### setShowHiddenText(boolean value) {#setShowHiddenText-boolean-}
```
public void setShowHiddenText(boolean value)
```


Устанавливает индикацию того, отображается ли скрытый текст в документе. По умолчанию — Ложь. Это свойство влияет на весь скрытый контент, а не только на текст.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Индикация того, отображается ли скрытый текст в документе. |

### setShowParagraphMarks(boolean value) {#setShowParagraphMarks-boolean-}
```
public void setShowParagraphMarks(boolean value)
```


Устанавливает индикацию того, отображаются ли метки абзаца. По умолчанию — Ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Индикация того, отображаются ли знаки абзаца. |

### setTextShaperFactory(ITextShaperFactory value) {#setTextShaperFactory-com.aspose.words.ITextShaperFactory-}
```
public void setTextShaperFactory(ITextShaperFactory value)
```


 Наборы[ITextShaperFactory](../../com.aspose.words/itextshaperfactory) реализация, используемая для функций рендеринга Advanced Typography.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory) | \{[ITextShaperFactory](../../com.aspose.words/itextshaperfactory) реализация, используемая для функций рендеринга Advanced Typography. |

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
