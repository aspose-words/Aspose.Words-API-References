---
title: Metered
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет методы для установки измеренного ключа.
type: docs
weight: 398
url: /ru/java/com.aspose.words/metered/
---

**Наследование:**
java.lang.Object
```
public class Metered
```

Предоставляет методы для установки измеренного ключа.

 Чтобы узнать больше, посетите**Licensing and Subscription** документальная статья.

В этом примере будет предпринята попытка установить измеренный открытый и закрытый ключ для jar-файла компонента:

```

 Metered matered = new Metered();
 matered.setMeteredKey("PublicKey", "PrivateKey");
 
```
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [Metered()](#Metered--) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getConsumptionCredit()](#getConsumptionCredit--) | Получает потребительский кредит |
| [getConsumptionQuantity()](#getConsumptionQuantity--) | Получает размер файла потребления |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setMeteredKey(String publicKey, String privateKey)](#setMeteredKey-java.lang.String-java.lang.String-) | Устанавливает измеренный открытый и закрытый ключ. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Metered() {#Metered--}
```
public Metered()
```


Инициализирует новый экземпляр этого класса.

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
### getConsumptionCredit() {#getConsumptionCredit--}
```
public static BigDecimal getConsumptionCredit()
```


Получает потребительский кредит

**Возвращает:**
java.math.BigDecimal - количество потребления
### getConsumptionQuantity() {#getConsumptionQuantity--}
```
public static BigDecimal getConsumptionQuantity()
```


Получает размер файла потребления

**Возвращает:**
java.math.BigDecimal - количество потребления
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




### setMeteredKey(String publicKey, String privateKey) {#setMeteredKey-java.lang.String-java.lang.String-}
```
public void setMeteredKey(String publicKey, String privateKey)
```


Устанавливает измеренный открытый и закрытый ключ. Если вы покупаете лимитную лицензию, при запуске приложения должен вызываться этот API, обычно этого достаточно. Однако, если всегда не удается загрузить данные о потреблении и превышает 24 часа, лицензия будет установлена в статус оценки, чтобы избежать этого, вы должны регулярно проверять статус лицензии, если это статус оценки, снова вызывать этот API.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| publicKey | java.lang.String | открытый ключ |
| privateKey | java.lang.String | закрытый ключ |

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
