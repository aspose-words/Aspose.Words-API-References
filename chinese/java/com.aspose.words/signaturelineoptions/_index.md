---
title: SignatureLineOptions
second_title: Aspose.Words for Java API 参考
description: 允许为插入的签名行指定选项。
type: docs
weight: 525
url: /zh/java/com.aspose.words/signaturelineoptions/
---

**遗产：**
java.lang.Object
```
public class SignatureLineOptions
```

允许为插入的签名行指定选项。用于[DocumentBuilder](../../com.aspose.words/documentbuilder).

要了解更多信息，请访问**Work with Digital Signatures**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAllowComments()](#getAllowComments--) | 获取一个值，该值指示签名者可以在“签名”对话框中添加注释。 |
| [getClass()](#getClass--) |  |
| [getDefaultInstructions()](#getDefaultInstructions--) | 获取一个值，该值指示默认说明显示在“签名”对话框中。 |
| [getEmail()](#getEmail--) | 获取建议的签名者的电子邮件地址。 |
| [getInstructions()](#getInstructions--) | 获取签名者在签署签名行时显示的说明。 |
| [getShowDate()](#getShowDate--) | 获取一个值，该值指示签名日期显示在签名行中。 |
| [getSigner()](#getSigner--) | 获取签名行的建议签名者。 |
| [getSignerTitle()](#getSignerTitle--) | 获取建议的签名者的头衔。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowComments(boolean value)](#setAllowComments-boolean-) | 设置一个值，指示签名者可以在“签名”对话框中添加注释。 |
| [setDefaultInstructions(boolean value)](#setDefaultInstructions-boolean-) | 设置一个值，指示默认指令显示在“签名”对话框中。 |
| [setEmail(String value)](#setEmail-java.lang.String-) | 设置建议的签名者的电子邮件地址。 |
| [setInstructions(String value)](#setInstructions-java.lang.String-) | 为签署签名行时显示的签名者设置说明。 |
| [setShowDate(boolean value)](#setShowDate-boolean-) | 设置一个值，指示签名日期显示在签名行中。 |
| [setSigner(String value)](#setSigner-java.lang.String-) | 设置签名行的建议签名者。 |
| [setSignerTitle(String value)](#setSignerTitle-java.lang.String-) | 设置建议的签名者的头衔。 |
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
### getAllowComments() {#getAllowComments--}
```
public boolean getAllowComments()
```


获取一个值，该值指示签名者可以在“签名”对话框中添加注释。此属性的默认值为**false**.

**退货：**
布尔值 - 一个值，指示签名者可以在“签名”对话框中添加评论。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getDefaultInstructions() {#getDefaultInstructions--}
```
public boolean getDefaultInstructions()
```


获取一个值，该值指示默认说明显示在“签名”对话框中。此属性的默认值为**true**.

**退货：**
布尔值 - 一个值，表示默认指令显示在“签名”对话框中。
### getEmail() {#getEmail--}
```
public String getEmail()
```


获取建议的签名者的电子邮件地址。此属性的默认值为**empty string**.

**退货：**
java.lang.String - 建议的签名者的电子邮件地址。
### getInstructions() {#getInstructions--}
```
public String getInstructions()
```


获取签名者在签署签名行时显示的说明。此属性的默认值为**empty string**.

**退货：**
java.lang.String - 在签署签名行时显示给签名者的说明。
### getShowDate() {#getShowDate--}
```
public boolean getShowDate()
```


获取一个值，该值指示签名日期显示在签名行中。此属性的默认值为**true**.

**退货：**
boolean - 指示签名日期显示在签名行中的值。
### getSigner() {#getSigner--}
```
public String getSigner()
```


获取签名行的建议签名者。此属性的默认值为**empty string**.

**退货：**
java.lang.String - 签名行的建议签名者。
### getSignerTitle() {#getSignerTitle--}
```
public String getSignerTitle()
```


获取建议的签名者的头衔。此属性的默认值为**empty string**.

**退货：**
java.lang.String - 建议的签名者的头衔。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAllowComments(boolean value) {#setAllowComments-boolean-}
```
public void setAllowComments(boolean value)
```


设置一个值，指示签名者可以在“签名”对话框中添加注释。此属性的默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示签名者可以在“签名”对话框中添加注释的值。 |

### setDefaultInstructions(boolean value) {#setDefaultInstructions-boolean-}
```
public void setDefaultInstructions(boolean value)
```


设置一个值，指示默认指令显示在“签名”对话框中。此属性的默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示默认指令的值显示在“签名”对话框中。 |

### setEmail(String value) {#setEmail-java.lang.String-}
```
public void setEmail(String value)
```


设置建议的签名者的电子邮件地址。此属性的默认值为**empty string**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 建议的签名者的电子邮件地址。 |

### setInstructions(String value) {#setInstructions-java.lang.String-}
```
public void setInstructions(String value)
```


为签署签名行时显示的签名者设置说明。此属性的默认值为**empty string**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 在签署签名行时显示给签名者的说明。 |

### setShowDate(boolean value) {#setShowDate-boolean-}
```
public void setShowDate(boolean value)
```


设置一个值，指示签名日期显示在签名行中。此属性的默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示签名日期的值显示在签名行中。 |

### setSigner(String value) {#setSigner-java.lang.String-}
```
public void setSigner(String value)
```


设置签名行的建议签名者。此属性的默认值为**empty string**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 签名行的建议签名者。 |

### setSignerTitle(String value) {#setSignerTitle-java.lang.String-}
```
public void setSignerTitle(String value)
```


设置建议的签名者的头衔。此属性的默认值为**empty string**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 建议的签名者的头衔。 |

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
