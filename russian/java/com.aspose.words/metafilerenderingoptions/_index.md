---
title: MetafileRenderingOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать дополнительные параметры рендеринга метафайла.
type: docs
weight: 397
url: /ru/java/com.aspose.words/metafilerenderingoptions/
---

**Наследование:**
java.lang.Object
```
public class MetafileRenderingOptions
```

Позволяет указать дополнительные параметры рендеринга метафайла.

 Чтобы узнать больше, посетите**Handling Windows Metafiles** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getEmfPlusDualRenderingMode()](#getEmfPlusDualRenderingMode--) | Получает значение, определяющее способ отображения метафайлов EMF+ Dual. |
| [getEmulateRasterOperations()](#getEmulateRasterOperations--) | Получает значение, определяющее, следует ли эмулировать растровые операции. |
| [getRenderingMode()](#getRenderingMode--) | Получает значение, определяющее способ отображения изображений метафайлов. |
| [getScaleWmfFontsToMetafileSize()](#getScaleWmfFontsToMetafileSize--) | Получает значение, определяющее, следует ли масштабировать шрифты в метафайле WMF в соответствии с размером метафайла на странице. |
| [getUseEmfEmbeddedToWmf()](#getUseEmfEmbeddedToWmf--) | Получает значение, определяющее способ отображения метафайлов WMF со встроенными метафайлами EMF. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setEmfPlusDualRenderingMode(int value)](#setEmfPlusDualRenderingMode-int-) | Задает значение, определяющее способ отображения метафайлов EMF+ Dual. |
| [setEmulateRasterOperations(boolean value)](#setEmulateRasterOperations-boolean-) | Задает значение, определяющее, следует ли эмулировать растровые операции. |
| [setRenderingMode(int value)](#setRenderingMode-int-) | Задает значение, определяющее, как должны отображаться изображения метафайлов. |
| [setScaleWmfFontsToMetafileSize(boolean value)](#setScaleWmfFontsToMetafileSize-boolean-) | Задает значение, определяющее, следует ли масштабировать шрифты в метафайле WMF в соответствии с размером метафайла на странице. |
| [setUseEmfEmbeddedToWmf(boolean value)](#setUseEmfEmbeddedToWmf-boolean-) | Задает значение, определяющее, как должны отображаться метафайлы WMF со встроенными метафайлами EMF. |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getEmfPlusDualRenderingMode() {#getEmfPlusDualRenderingMode--}
```
public int getEmfPlusDualRenderingMode()
```


Получает значение, определяющее способ отображения метафайлов EMF+ Dual.

Двойные метафайлы EMF+ содержат как части EMF+, так и части EMF. MS Word и GDI+ всегда отображают часть EMF+. В настоящее время Aspose.Words не полностью поддерживает все записи EMF+, и в некоторых случаях результат рендеринга части EMF выглядит лучше, чем результат рендеринга части EMF+.

Этот параметр используется только тогда, когда метафайл визуализируется как векторная графика. Когда метафайл преобразуется в растровое изображение, всегда используется часть EMF+.

 Значение по умолчанию[EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode\#EMF-PLUS-WITH-FALLBACK).

**Возвращает:**
 int — значение, определяющее способ отображения метафайлов EMF+ Dual. Возвращаемое значение является одним из[EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode) константы.
### getEmulateRasterOperations() {#getEmulateRasterOperations--}
```
public boolean getEmulateRasterOperations()
```


Получает значение, определяющее, следует ли эмулировать растровые операции.

В метафайлах можно использовать определенные растровые операции. Их нельзя визуализировать напрямую в векторную графику. Эмуляция растровых операций требует частичной растеризации результирующей векторной графики, что может повлиять на производительность рендеринга метафайлов.

Когда для этого значения установлено значение true , Aspose.Words эмулирует растровые операции. Полученный результат может быть частично растрирован, и производительность может снизиться.

Когда для этого значения установлено значение false , Aspose.Words не эмулирует растровые операции. Когда Aspose.Words встречает растровую операцию в метафайле, он переходит к рендерингу метафайла в растровое изображение с помощью операционной системы.

Этот параметр используется только тогда, когда метафайл визуализируется как векторная графика.

Значение по умолчанию верно .

**Возвращает:**
boolean — значение, определяющее, следует ли эмулировать растровые операции.
### getRenderingMode() {#getRenderingMode--}
```
public int getRenderingMode()
```


Получает значение, определяющее способ отображения изображений метафайлов.

 Значение по умолчанию зависит от формата сохранения. Для изображений это[MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP) . Для других форматов это[MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode\#VECTOR-WITH-FALLBACK).

**Возвращает:**
 int — значение, определяющее, как должны отображаться изображения метафайлов. Возвращаемое значение является одним из[MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode) константы.
### getScaleWmfFontsToMetafileSize() {#getScaleWmfFontsToMetafileSize--}
```
public boolean getScaleWmfFontsToMetafileSize()
```


Получает значение, определяющее, следует ли масштабировать шрифты в метафайле WMF в соответствии с размером метафайла на странице.

Когда метафайлы WMF отображаются в MS Word, шрифты могут масштабироваться в соответствии с фактическим размером метафайла на странице.

Когда для этого значения установлено значение true , Aspose.Words эмулирует масштабирование шрифта в соответствии с размером метафайла на странице.

Когда для этого значения установлено значение false , Aspose.Words отображает шрифты, поскольку метафайл отображается с размером по умолчанию.

Этот параметр используется только тогда, когда метафайл визуализируется как векторная графика.

Значение по умолчанию верно .

**Возвращает:**
логическое значение — значение, определяющее, следует ли масштабировать шрифты в метафайле WMF в соответствии с размером метафайла на странице.
### getUseEmfEmbeddedToWmf() {#getUseEmfEmbeddedToWmf--}
```
public boolean getUseEmfEmbeddedToWmf()
```


Получает значение, определяющее способ отображения метафайлов WMF со встроенными метафайлами EMF.

Метафайлы WMF могут содержать встроенные данные EMF. MS Word в большинстве случаев использует встроенные данные EMF. GDI+ всегда использует данные WMF.

Когда для этого значения установлено значение true , Aspose.Words использует встроенные данные EMF при рендеринге.

Когда для этого значения установлено значение false , Aspose.Words использует данные WMF при рендеринге.

Этот параметр используется только тогда, когда метафайл визуализируется как векторная графика. Когда метафайл преобразуется в растровое изображение, всегда используются данные WMF.

Значение по умолчанию верно .

**Возвращает:**
boolean — значение, определяющее, как должны отображаться метафайлы WMF со встроенными метафайлами EMF.
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




### setEmfPlusDualRenderingMode(int value) {#setEmfPlusDualRenderingMode-int-}
```
public void setEmfPlusDualRenderingMode(int value)
```


Задает значение, определяющее способ отображения метафайлов EMF+ Dual.

Двойные метафайлы EMF+ содержат как части EMF+, так и части EMF. MS Word и GDI+ всегда отображают часть EMF+. В настоящее время Aspose.Words не полностью поддерживает все записи EMF+, и в некоторых случаях результат рендеринга части EMF выглядит лучше, чем результат рендеринга части EMF+.

Этот параметр используется только тогда, когда метафайл визуализируется как векторная графика. Когда метафайл преобразуется в растровое изображение, всегда используется часть EMF+.

 Значение по умолчанию[EmfPlusDualRenderingMode.EMF\_PLUS\_WITH\_FALLBACK](../../com.aspose.words/emfplusdualrenderingmode\#EMF-PLUS-WITH-FALLBACK).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее способ отображения метафайлов EMF+ Dual. Значение должно быть одним из[EmfPlusDualRenderingMode](../../com.aspose.words/emfplusdualrenderingmode) константы. |

### setEmulateRasterOperations(boolean value) {#setEmulateRasterOperations-boolean-}
```
public void setEmulateRasterOperations(boolean value)
```


Задает значение, определяющее, следует ли эмулировать растровые операции.

В метафайлах можно использовать определенные растровые операции. Их нельзя визуализировать напрямую в векторную графику. Эмуляция растровых операций требует частичной растеризации результирующей векторной графики, что может повлиять на производительность рендеринга метафайлов.

Когда для этого значения установлено значение true , Aspose.Words эмулирует растровые операции. Полученный результат может быть частично растрирован, и производительность может снизиться.

Когда для этого значения установлено значение false , Aspose.Words не эмулирует растровые операции. Когда Aspose.Words встречает растровую операцию в метафайле, он переходит к рендерингу метафайла в растровое изображение с помощью операционной системы.

Этот параметр используется только тогда, когда метафайл визуализируется как векторная графика.

Значение по умолчанию верно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли эмулировать растровые операции. |

### setRenderingMode(int value) {#setRenderingMode-int-}
```
public void setRenderingMode(int value)
```


Задает значение, определяющее, как должны отображаться изображения метафайлов.

 Значение по умолчанию зависит от формата сохранения. Для изображений это[MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP) . Для других форматов это[MetafileRenderingMode.VECTOR\_WITH\_FALLBACK](../../com.aspose.words/metafilerenderingmode\#VECTOR-WITH-FALLBACK).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Значение, определяющее, как должны отображаться изображения метафайлов. Значение должно быть одним из[MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode) константы. |

### setScaleWmfFontsToMetafileSize(boolean value) {#setScaleWmfFontsToMetafileSize-boolean-}
```
public void setScaleWmfFontsToMetafileSize(boolean value)
```


Задает значение, определяющее, следует ли масштабировать шрифты в метафайле WMF в соответствии с размером метафайла на странице.

Когда метафайлы WMF отображаются в MS Word, шрифты могут масштабироваться в соответствии с фактическим размером метафайла на странице.

Когда для этого значения установлено значение true , Aspose.Words эмулирует масштабирование шрифта в соответствии с размером метафайла на странице.

Когда для этого значения установлено значение false , Aspose.Words отображает шрифты, поскольку метафайл отображается с размером по умолчанию.

Этот параметр используется только тогда, когда метафайл визуализируется как векторная графика.

Значение по умолчанию верно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли масштабировать шрифты в метафайле WMF в соответствии с размером метафайла на странице. |

### setUseEmfEmbeddedToWmf(boolean value) {#setUseEmfEmbeddedToWmf-boolean-}
```
public void setUseEmfEmbeddedToWmf(boolean value)
```


Задает значение, определяющее, как должны отображаться метафайлы WMF со встроенными метафайлами EMF.

Метафайлы WMF могут содержать встроенные данные EMF. MS Word в большинстве случаев использует встроенные данные EMF. GDI+ всегда использует данные WMF.

Когда для этого значения установлено значение true , Aspose.Words использует встроенные данные EMF при рендеринге.

Когда для этого значения установлено значение false , Aspose.Words использует данные WMF при рендеринге.

Этот параметр используется только тогда, когда метафайл визуализируется как векторная графика. Когда метафайл преобразуется в растровое изображение, всегда используются данные WMF.

Значение по умолчанию верно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, как должны отображаться метафайлы WMF со встроенными метафайлами EMF. |

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
