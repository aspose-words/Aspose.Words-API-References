---
title: NodeChangingArgs
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет данные для методов интерфейса.
type: docs
weight: 403
url: /ru/java/com.aspose.words/nodechangingargs/
---

**Наследование:**
java.lang.Object
```
public class NodeChangingArgs
```

 Предоставляет данные для методов[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) интерфейс.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAction()](#getAction--) | Получает значение, указывающее, какой тип события изменения узла происходит. |
| [getClass()](#getClass--) |  |
| [getNewParent()](#getNewParent--) | Получает родителя узла, который будет установлен после завершения операции. |
| [getNode()](#getNode--) |  Получает[getNode()](../../com.aspose.words/nodechangingargs\#getNode--) который добавляется или удаляется. |
| [getOldParent()](#getOldParent--) | Получает родителя узла до начала операции. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
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
### getAction() {#getAction--}
```
public int getAction()
```


Получает значение, указывающее, какой тип события изменения узла происходит.

**Возвращает:**
 int — значение, указывающее, какой тип события изменения узла происходит. Возвращаемое значение является одним из[NodeChangingAction](../../com.aspose.words/nodechangingaction) константы.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getNewParent() {#getNewParent--}
```
public Node getNewParent()
```


Получает родителя узла, который будет установлен после завершения операции.

**Возвращает:**
[Node](../../com.aspose.words/node) - Родитель узла, который будет установлен после завершения операции.
### getNode() {#getNode--}
```
public Node getNode()
```


 Получает[getNode()](../../com.aspose.words/nodechangingargs\#getNode--) который добавляется или удаляется.

**Возвращает:**
[Node](../../com.aspose.words/node) -[getNode()](../../com.aspose.words/nodechangingargs\#getNode--) который добавляется или удаляется.
### getOldParent() {#getOldParent--}
```
public Node getOldParent()
```


Получает родителя узла до начала операции.

**Возвращает:**
[Node](../../com.aspose.words/node) - Родитель узла до начала операции.
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
