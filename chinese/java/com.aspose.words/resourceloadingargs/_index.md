---
title: ResourceLoadingArgs
second_title: Aspose.Words for Java API 参考
description: 为方法提供数据。
type: docs
weight: 480
url: /zh/java/com.aspose.words/resourceloadingargs/
---

**遗产:**
java.lang.Object
```
public class ResourceLoadingArgs
```

提供数据为[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-)方法。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getOriginalUri()](#getOriginalUri--) | 导入文档中指定的资源的原始 URI。 |
| [getResourceType()](#getResourceType--) | 资源类型。 |
| [getUri()](#getUri--) | 用于下载的资源的 URI if[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-)返回[ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT). |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setData(byte[] data)](#setData-byte---) | 设置用户提供的资源数据，如果[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-)返回[ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction\#USER-PROVIDED). |
| [setUri(String value)](#setUri-java.lang.String-) | 用于下载的资源的 URI if[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-)返回[ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT). |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getOriginalUri() {#getOriginalUri--}
```
public String getOriginalUri()
```


导入文档中指定的资源的原始 URI。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getResourceType() {#getResourceType--}
```
public int getResourceType()
```


资源类型。

**退货:**
int - 对应的 int 值。返回值是以下之一[ResourceType](../../com.aspose.words/resourcetype)常数。
### getUri() {#getUri--}
```
public String getUri()
```


用于下载的资源的 URI if[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-)返回[ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT).

最初它设置为资源的绝对 URI，但用户可以将其重新定义为任何值。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
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


设置用户提供的资源数据，如果[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-)返回[ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction\#USER-PROVIDED).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| data | byte[] |  |

### setUri(String value) {#setUri-java.lang.String-}
```
public void setUri(String value)
```


用于下载的资源的 URI if[IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-)返回[ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction\#DEFAULT).

最初它设置为资源的绝对 URI，但用户可以将其重新定义为任何值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

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
