---
title: SignatureLine
second_title: Aspose.Words for Java API 参考
description: 提供对签名行属性的访问。
type: docs
weight: 524
url: /zh/java/com.aspose.words/signatureline/
---

**遗产：**
java.lang.Object
```
public class SignatureLine
```

提供对签名行属性的访问。

要了解更多信息，请访问**Work with Digital Signatures**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAllowComments()](#getAllowComments--) | 获取一个值，该值指示签名者可以在“签名”对话框中添加注释。 |
| [getClass()](#getClass--) |  |
| [getDefaultInstructions()](#getDefaultInstructions--) | 获取一个值，该值指示默认说明显示在“签名”对话框中。 |
| [getEmail()](#getEmail--) | 获取建议的签名者的电子邮件地址。 |
| [getId()](#getId--) | 获取此签名行的标识符。 |
| [getInstructions()](#getInstructions--) | 获取签名者在签署签名行时显示的说明。 |
| [getProviderId()](#getProviderId--) | 获取此签名行的签名提供程序标识符。 |
| [getShowDate()](#getShowDate--) | 获取一个值，该值指示签名日期显示在签名行中。 |
| [getSigner()](#getSigner--) | 获取签名行的建议签名者。 |
| [getSignerTitle()](#getSignerTitle--) | 获取建议的签名者的头衔（例如，经理）。 |
| [hashCode()](#hashCode--) |  |
| [isSigned()](#isSigned--) | 指示签名行由数字签名签名。 |
| [isValid()](#isValid--) | 表示签名行是经过数字签名签名的，并且这个数字签名是有效的。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowComments(boolean value)](#setAllowComments-boolean-) | 设置一个值，指示签名者可以在“签名”对话框中添加注释。 |
| [setDefaultInstructions(boolean value)](#setDefaultInstructions-boolean-) | 设置一个值，指示默认指令显示在“签名”对话框中。 |
| [setEmail(String value)](#setEmail-java.lang.String-) | 设置建议的签名者的电子邮件地址。 |
| [setId(UUID value)](#setId-java.util.UUID-) | 设置此签名行的标识符。 |
| [setInstructions(String value)](#setInstructions-java.lang.String-) | 为签署签名行时显示的签名者设置说明。 |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID-) | 为此签名行设置签名提供者标识符。 |
| [setShowDate(boolean value)](#setShowDate-boolean-) | 设置一个值，指示签名日期显示在签名行中。 |
| [setSigner(String value)](#setSigner-java.lang.String-) | 设置签名行的建议签名者。 |
| [setSignerTitle(String value)](#setSignerTitle-java.lang.String-) | 设置建议的签名者的头衔（例如，经理）。 |
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
### getId() {#getId--}
```
public UUID getId()
```


获取此签名行的标识符。

在使用签名文档时，此标识符可以与数字签名相关联[DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil).该值必须是唯一的，默认情况下它是随机生成的新 Guid。

**退货：**
java.util.UUID - 此签名行的标识符。
### getInstructions() {#getInstructions--}
```
public String getInstructions()
```


获取签名者在签署签名行时显示的说明。如果[getDefaultInstructions()](../../com.aspose.words/signatureline\#getDefaultInstructions--) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline\#setDefaultInstructions-boolean-)已设置。此属性的默认值为**empty string**.

**退货：**
java.lang.String - 在签署签名行时显示给签名者的说明。
### getProviderId() {#getProviderId--}
```
public UUID getProviderId()
```


获取此签名行的签名提供程序标识符。默认值为“\{00000000-0000-0000-0000-000000000000\}”。

加密服务提供者 (CSP) 是一个独立的软件模块，它实际上执行用于身份验证、编码和加密的加密算法。 MS Office 保留的价值\{00000000-0000-0000-0000-000000000000\为其默认签名提供者。

额外安装的提供程序的 GUID 应从提供程序随附的文档中获取。

此外，所有已安装的加密提供程序都在 Windows 注册表中枚举。可以在以下路径中找到：HKLM\\软件\\微软\\密码学\\默认值\\提供者。有一个密钥名称“CP Service UUID”，它对应于签名提供者的 GUID。

**退货：**
java.util.UUID - 此签名行的签名提供者标识符。
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


获取建议的签名者的头衔（例如，经理）。此属性的默认值为**empty string**.

**退货：**
java.lang.String - 建议的签名者头衔（例如，经理）。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### isSigned() {#isSigned--}
```
public boolean isSigned()
```


指示签名行由数字签名签名。

**退货：**
boolean - 相应的布尔值。
### isValid() {#isValid--}
```
public boolean isValid()
```


表示签名行是经过数字签名签名的，并且这个数字签名是有效的。

**退货：**
boolean - 相应的布尔值。
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

### setId(UUID value) {#setId-java.util.UUID-}
```
public void setId(UUID value)
```


设置此签名行的标识符。

在使用签名文档时，此标识符可以与数字签名相关联[DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil).该值必须是唯一的，默认情况下它是随机生成的新 Guid。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.UUID | 此签名行的标识符。 |

### setInstructions(String value) {#setInstructions-java.lang.String-}
```
public void setInstructions(String value)
```


为签署签名行时显示的签名者设置说明。如果[getDefaultInstructions()](../../com.aspose.words/signatureline\#getDefaultInstructions--) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline\#setDefaultInstructions-boolean-)已设置。此属性的默认值为**empty string**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 在签署签名行时显示给签名者的说明。 |

### setProviderId(UUID value) {#setProviderId-java.util.UUID-}
```
public void setProviderId(UUID value)
```


为此签名行设置签名提供者标识符。默认值为“\{00000000-0000-0000-0000-000000000000\}”。

加密服务提供者 (CSP) 是一个独立的软件模块，它实际上执行用于身份验证、编码和加密的加密算法。 MS Office 保留的价值\{00000000-0000-0000-0000-000000000000\为其默认签名提供者。

额外安装的提供程序的 GUID 应从提供程序随附的文档中获取。

此外，所有已安装的加密提供程序都在 Windows 注册表中枚举。可以在以下路径中找到：HKLM\\软件\\微软\\密码学\\默认值\\提供者。有一个密钥名称“CP Service UUID”，它对应于签名提供者的 GUID。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.UUID | 此签名行的签名提供程序标识符。 |

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


设置建议的签名者的头衔（例如，经理）。此属性的默认值为**empty string**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 建议的签名者职位（例如，经理）。 |

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
