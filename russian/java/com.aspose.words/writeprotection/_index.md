---
title: WriteProtection
second_title: Справочник по API Aspose.Words для Java
description: Указывает параметры защиты от записи для документа.
type: docs
weight: 623
url: /ru/java/com.aspose.words/writeprotection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class WriteProtection implements Cloneable
```

Указывает параметры защиты от записи для документа.

 Чтобы узнать больше, посетите**Protect or Encrypt a Document** документальная статья.

Защита от записи указывает, рекомендовал ли автор открывать документ только для чтения и/или требовать пароль для изменения документа.

Защита от записи отличается от защиты документа. Защита от записи указывается в Microsoft Word в параметрах диалогового окна «Сохранить как».

 Вы не создаете экземпляры этого класса напрямую. Доступ к настройкам защиты документов осуществляется через[Document.getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--) имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getReadOnlyRecommended()](#getReadOnlyRecommended--) | Указывает, рекомендовал ли автор документа открывать документ только для чтения. |
| [hashCode()](#hashCode--) |  |
| [isWriteProtected()](#isWriteProtected--) | Возвращает true, если установлен пароль защиты от записи. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setPassword(String password)](#setPassword-java.lang.String-) | Устанавливает пароль защиты от записи для документа. |
| [setReadOnlyRecommended(boolean value)](#setReadOnlyRecommended-boolean-) | Указывает, рекомендовал ли автор документа открывать документ только для чтения. |
| [toString()](#toString--) |  |
| [validatePassword(String password)](#validatePassword-java.lang.String-) | Возвращает true, если указанный пароль совпадает с паролем защиты от записи, которым был защищен документ. |
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
### getReadOnlyRecommended() {#getReadOnlyRecommended--}
```
public boolean getReadOnlyRecommended()
```


Указывает, рекомендовал ли автор документа открывать документ только для чтения.

**Возвращает:**
boolean - соответствующее логическое значение.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isWriteProtected() {#isWriteProtected--}
```
public boolean isWriteProtected()
```


Возвращает true, если установлен пароль защиты от записи.

**Возвращает:**
boolean — True, если установлен пароль защиты от записи.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setPassword(String password) {#setPassword-java.lang.String-}
```
public void setPassword(String password)
```


Устанавливает пароль защиты от записи для документа.

Если установлен пароль, Microsoft Word потребует от пользователя ввести его или открыть документ только для чтения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| password | java.lang.String | Пароль для установки. Не может быть нулевым, но может быть пустой строкой. |

### setReadOnlyRecommended(boolean value) {#setReadOnlyRecommended-boolean-}
```
public void setReadOnlyRecommended(boolean value)
```


Указывает, рекомендовал ли автор документа открывать документ только для чтения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### validatePassword(String password) {#validatePassword-java.lang.String-}
```
public boolean validatePassword(String password)
```


Возвращает true, если указанный пароль совпадает с паролем защиты от записи, которым был защищен документ. Если документ не защищен паролем от записи, возвращается false.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| password | java.lang.String |  |

**Возвращает:**
логический
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
