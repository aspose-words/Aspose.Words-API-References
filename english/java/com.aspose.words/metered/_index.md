---
title: Metered
second_title: Aspose.Words for Java API 参考
description: 提供设置计量键的方法。
type: docs
weight: 398
url: /zh/java/com.aspose.words/metered/
---

**遗产:**
java.lang.Object
```
public class Metered
```

提供设置计量键的方法。

要了解更多信息，请访问**Licensing and Subscription**文档文章。

在此示例中，将尝试为组件 jar 文件设置计量的公钥和私钥：

```

 Metered matered = new Metered();
 matered.setMeteredKey("PublicKey", "PrivateKey");
 
```
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [Metered()](#Metered--) | 初始化此类的新实例。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getConsumptionCredit()](#getConsumptionCredit--) | 获得消费积分 |
| [getConsumptionQuantity()](#getConsumptionQuantity--) | 获取消费文件大小 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setMeteredKey(String publicKey, String privateKey)](#setMeteredKey-java.lang.String-java.lang.String-) | 设置计量的公钥和私钥。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Metered() {#Metered--}
```
public Metered()
```


初始化此类的新实例。

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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getConsumptionCredit() {#getConsumptionCredit--}
```
public static BigDecimal getConsumptionCredit()
```


获得消费积分

**退货:**
java.math.BigDecimal - 消费数量
### getConsumptionQuantity() {#getConsumptionQuantity--}
```
public static BigDecimal getConsumptionQuantity()
```


获取消费文件大小

**退货:**
java.math.BigDecimal - 消费数量
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




### setMeteredKey(String publicKey, String privateKey) {#setMeteredKey-java.lang.String-java.lang.String-}
```
public void setMeteredKey(String publicKey, String privateKey)
```


设置计量的公钥和私钥。如果您购买的是计量许可证，在启动应用程序时，应该调用此 API，正常情况下，这就足够了。但是，如果总是无法上传消费数据，超过24小时，License会被设置为评估状态，为避免这种情况，您应该定期检查License状态，如果是评估状态，再次调用该API。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| publicKey | java.lang.String | 公钥 |
| privateKey | java.lang.String | 私钥 |

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
