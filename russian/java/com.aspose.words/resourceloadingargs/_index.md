---
title: ResourceLoadingArgs
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет данные для метода.
type: docs
weight: 480
url: /ru/java/com.aspose.words/resourceloadingargs/
---

**Наследование:**
java.lang.Object
```
public class ResourceLoadingArgs
```

 Предоставляет данные для[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) метод.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getOriginalUri()](#getOriginalUri--) | Исходный URI ресурса, указанный в импортированном документе. |
| [getResourceType()](#getResourceType--) | Тип ресурса. |
| [getUri()](#getUri--) |  URI ресурса, который используется для скачивания, если[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) возвращается[ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT). |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setData(byte[] data)](#setData-byte---) |  Устанавливает предоставленные пользователем данные ресурса, который используется, если[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) возвращается[ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction\#USER-PROVIDED). |
| [setUri(String value)](#setUri-java.lang.String-) |  URI ресурса, который используется для скачивания, если[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) возвращается[ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT). |
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
### getOriginalUri() {#getOriginalUri--}
```
public String getOriginalUri()
```


Исходный URI ресурса, указанный в импортированном документе.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getResourceType() {#getResourceType--}
```
public int getResourceType()
```


Тип ресурса.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ResourceType](../../com.aspose.words/resourcetype) константы.
### getUri() {#getUri--}
```
public String getUri()
```


 URI ресурса, который используется для скачивания, если[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) возвращается[ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT).

Изначально он установлен как абсолютный URI ресурса, но пользователь может переопределить его на любое значение.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
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




### setData(byte[] data) {#setData-byte---}
```
public void setData(byte[] data)
```


 Устанавливает предоставленные пользователем данные ресурса, который используется, если[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) возвращается[ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction\#USER-PROVIDED).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| data | byte[] |  |

### setUri(String value) {#setUri-java.lang.String-}
```
public void setUri(String value)
```


 URI ресурса, который используется для скачивания, если[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) возвращается[ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT).

Изначально он установлен как абсолютный URI ресурса, но пользователь может переопределить его на любое значение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

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
