---
title: LayoutEnumerator
second_title: Справочник по API Aspose.Words для Java
description: Перечисляет объекты макета страницы документа.
type: docs
weight: 360
url: /ru/java/com.aspose.words/layoutenumerator/
---

**Наследование:**
java.lang.Object
```
public class LayoutEnumerator
```

 Перечисляет объекты макета страницы документа. Вы можете использовать этот класс для просмотра модели макета страницы. Доступными свойствами являются тип, геометрия, текст и индекс страницы, на которой отображается объект, а также общая структура и отношения. Используйте комбинацию[LayoutCollector.getEntity(com.aspose.words.Node)](../../com.aspose.words/layoutcollector\#getEntity-com.aspose.words.Node-) а также[getCurrent()](../../com.aspose.words/layoutenumerator\#getCurrent--) / [setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator\#setCurrent-java.lang.Object-) перейти к объекту, который соответствует узлу документа.

 Чтобы узнать больше, посетите**Converting to Fixed-page Format** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [LayoutEnumerator(Document document)](#LayoutEnumerator-com.aspose.words.Document-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(String key)](#get-java.lang.String-) | Получает именованное свойство объекта. |
| [getClass()](#getClass--) |  |
| [getCurrent()](#getCurrent--) | Получает текущую позицию в модели макета страницы. |
| [getDocument()](#getDocument--) | Получает документ, перечисляемый этим экземпляром. |
| [getKind()](#getKind--) | Получает вид текущей сущности. |
| [getPageIndex()](#getPageIndex--) | Получает отсчитываемый от 1 индекс страницы, содержащей текущий объект. |
| [getRectangle()](#getRectangle--) | Возвращает ограничивающий прямоугольник текущего объекта относительно верхнего левого угла страницы (в пунктах). |
| [getText()](#getText--) | Получает текст текущего объекта диапазона. |
| [getType()](#getType--) | Получает тип текущей сущности. |
| [hashCode()](#hashCode--) |  |
| [moveFirstChild()](#moveFirstChild--) | Переходит к первому дочернему объекту. |
| [moveLastChild()](#moveLastChild--) | Переходит к последнему дочернему объекту. |
| [moveNext()](#moveNext--) | Переходит к следующему родственному объекту в визуальном порядке. |
| [moveNextLogical()](#moveNextLogical--) | Переходит к следующему одноуровневому объекту в логическом порядке. |
| [moveParent()](#moveParent--) | Перемещается к родительскому объекту. |
| [moveParent(int types)](#moveParent-int-) |  |
| [movePrevious()](#movePrevious--) | Переходит к предыдущему родственному объекту. |
| [movePreviousLogical()](#movePreviousLogical--) | Переходит к предыдущему одноуровневому объекту в логическом порядке. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [reset()](#reset--) | Перемещает перечислитель на первую страницу документа. |
| [setCurrent(Object value)](#setCurrent-java.lang.Object-) | Устанавливает текущую позицию в модели макета страницы. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### LayoutEnumerator(Document document) {#LayoutEnumerator-com.aspose.words.Document-}
```
public LayoutEnumerator(Document document)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | Документ, модель макета страницы которого необходимо перечислить.

 Если модель макета страницы документа не была построена, перечислитель вызывает[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) построить его.

 Всякий раз, когда документ обновляется и создается новая модель макета страницы, для доступа к ней необходимо использовать новый перечислитель.|

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
### get(String key) {#get-java.lang.String-}
```
public Object get(String key)
```


Получает именованное свойство объекта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | java.lang.String | Имя свойства (с учетом регистра). |

**Возвращает:**
java.lang.Object — Null, если свойство недоступно, в противном случае — значение свойства. В настоящее время это используется для получения свойств шрифта диапазонов. Видеть[Font](../../com.aspose.words/font) class для возможных имен свойств. Поддерживаются не все свойства.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCurrent() {#getCurrent--}
```
public Object getCurrent()
```


Получает текущую позицию в модели макета страницы. Это свойство возвращает непрозрачный объект, соответствующий текущему объекту макета.

**Возвращает:**
java.lang.Object — Текущая позиция в модели макета страницы.
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Получает документ, перечисляемый этим экземпляром.

**Возвращает:**
[Document](../../com.aspose.words/document) - Документ перечисляет этот экземпляр.
### getKind() {#getKind--}
```
public String getKind()
```


 Получает вид текущей сущности. Это может быть пустая строка, но не null. Это более конкретный тип текущего объекта, например, диапазон закладок имеет[LayoutEntityType.SPAN](../../com.aspose.words/layoutentitytype\#SPAN) тип и может иметь вид BOOKMARKSTART или BOOKMARKEND.

**Возвращает:**
java.lang.String — вид текущего объекта.
### getPageIndex() {#getPageIndex--}
```
public int getPageIndex()
```


Получает отсчитываемый от 1 индекс страницы, содержащей текущий объект.

**Возвращает:**
int — индекс страницы, начинающийся с 1 и содержащий текущий объект.
### getRectangle() {#getRectangle--}
```
public Rectangle2D.Float getRectangle()
```


Возвращает ограничивающий прямоугольник текущего объекта относительно верхнего левого угла страницы (в пунктах).

**Возвращает:**
java.awt.geom.Rectangle2D.Float — ограничивающий прямоугольник текущего объекта относительно верхнего левого угла страницы (в пунктах).
### getText() {#getText--}
```
public String getText()
```


Получает текст текущего объекта диапазона. Броски для других типов сущностей.

**Возвращает:**
java.lang.String — текст текущего объекта диапазона.
### getType() {#getType--}
```
public int getType()
```


Получает тип текущей сущности.

**Возвращает:**
 int - Тип текущего объекта. Возвращаемое значение представляет собой побитовую комбинацию[LayoutEntityType](../../com.aspose.words/layoutentitytype) константы.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### moveFirstChild() {#moveFirstChild--}
```
public boolean moveFirstChild()
```


Переходит к первому дочернему объекту.

**Возвращает:**
логический
### moveLastChild() {#moveLastChild--}
```
public boolean moveLastChild()
```


Переходит к последнему дочернему объекту.

**Возвращает:**
логический
### moveNext() {#moveNext--}
```
public boolean moveNext()
```


Переходит к следующему родственному объекту в визуальном порядке. При повторении строк абзаца, разбитых на страницы, этот метод не будет переходить на следующую страницу, а скорее перейдет к следующему объекту на той же странице.

**Возвращает:**
логический
### moveNextLogical() {#moveNextLogical--}
```
public boolean moveNextLogical()
```


 Переходит к следующему одноуровневому объекту в логическом порядке. При повторении строк абзаца, разбитых на страницы, этот метод перейдет к следующей строке, даже если она находится на другой странице. Обратите внимание, что все[LayoutEntityType.SPAN](../../com.aspose.words/layoutentitytype\#SPAN) объекты связаны друг с другом таким образом, если[getCurrent()](../../com.aspose.words/layoutenumerator\#getCurrent--) / [setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator\#setCurrent-java.lang.Object-) объект охватывает повторный вызов этого метода, который будет повторять полную историю документа.

**Возвращает:**
логический
### moveParent() {#moveParent--}
```
public boolean moveParent()
```


Перемещается к родительскому объекту.

**Возвращает:**
логический
### moveParent(int types) {#moveParent-int-}
```
public boolean moveParent(int types)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| types | int |  |

**Возвращает:**
логический
### movePrevious() {#movePrevious--}
```
public boolean movePrevious()
```


Переходит к предыдущему родственному объекту.

**Возвращает:**
логический
### movePreviousLogical() {#movePreviousLogical--}
```
public boolean movePreviousLogical()
```


 Переходит к предыдущему одноуровневому объекту в логическом порядке. При повторении строк абзаца, разбитых на страницы, этот метод переместится на предыдущую строку, даже если она находится на другой странице. Обратите внимание, что все[LayoutEntityType.SPAN](../../com.aspose.words/layoutentitytype\#SPAN) объекты связаны друг с другом таким образом, если[getCurrent()](../../com.aspose.words/layoutenumerator\#getCurrent--) / [setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator\#setCurrent-java.lang.Object-) объект охватывает повторный вызов этого метода, который будет повторять полную историю документа.

**Возвращает:**
логический
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### reset() {#reset--}
```
public void reset()
```


Перемещает перечислитель на первую страницу документа.

### setCurrent(Object value) {#setCurrent-java.lang.Object-}
```
public void setCurrent(Object value)
```


Устанавливает текущую позицию в модели макета страницы. Это свойство возвращает непрозрачный объект, соответствующий текущему объекту макета.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.Object | Текущая позиция в модели макета страницы. |

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
