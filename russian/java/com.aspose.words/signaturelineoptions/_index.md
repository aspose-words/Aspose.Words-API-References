---
title: SignatureLineOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать параметры для вставляемой строки подписи.
type: docs
weight: 525
url: /ru/java/com.aspose.words/signaturelineoptions/
---

**Наследование:**
java.lang.Object
```
public class SignatureLineOptions
```

 Позволяет указать параметры для вставляемой строки подписи. Используется в[DocumentBuilder](../../com.aspose.words/documentbuilder).

 Чтобы узнать больше, посетите**Work with Digital Signatures** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAllowComments()](#getAllowComments--) | Получает значение, указывающее, что подписывающая сторона может добавлять комментарии в диалоговом окне «Подписать». |
| [getClass()](#getClass--) |  |
| [getDefaultInstructions()](#getDefaultInstructions--) | Получает значение, указывающее, что инструкции по умолчанию отображаются в диалоговом окне Sign. |
| [getEmail()](#getEmail--) | Получает предполагаемый адрес электронной почты подписывающей стороны. |
| [getInstructions()](#getInstructions--) | Получает инструкции для подписывающей стороны, которые отображаются при подписании строки подписи. |
| [getShowDate()](#getShowDate--) | Получает значение, указывающее, что дата подписи отображается в строке подписи. |
| [getSigner()](#getSigner--) | Получает предполагаемого подписывающего в строке подписи. |
| [getSignerTitle()](#getSignerTitle--) | Получает предложенный титул подписывающей стороны. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowComments(boolean value)](#setAllowComments-boolean-) | Задает значение, указывающее, что подписывающая сторона может добавлять комментарии в диалоговом окне «Подписать». |
| [setDefaultInstructions(boolean value)](#setDefaultInstructions-boolean-) | Задает значение, указывающее, что в диалоговом окне «Подпись» отображаются инструкции по умолчанию. |
| [setEmail(String value)](#setEmail-java.lang.String-) | Устанавливает предполагаемый адрес электронной почты подписывающей стороны. |
| [setInstructions(String value)](#setInstructions-java.lang.String-) | Задает инструкции для подписывающей стороны, которые отображаются при подписании строки подписи. |
| [setShowDate(boolean value)](#setShowDate-boolean-) | Задает значение, указывающее, что дата подписи отображается в строке подписи. |
| [setSigner(String value)](#setSigner-java.lang.String-) | Устанавливает предполагаемого подписывающего в строке подписи. |
| [setSignerTitle(String value)](#setSignerTitle-java.lang.String-) | Устанавливает предполагаемый титул подписавшего. |
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
### getAllowComments() {#getAllowComments--}
```
public boolean getAllowComments()
```


 Получает значение, указывающее, что подписывающая сторона может добавлять комментарии в диалоговом окне «Подписать». Значение по умолчанию для этого свойства**false**.

**Возвращает:**
boolean — значение, указывающее, что подписывающая сторона может добавлять комментарии в диалоговом окне «Подписать».
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDefaultInstructions() {#getDefaultInstructions--}
```
public boolean getDefaultInstructions()
```


 Получает значение, указывающее, что инструкции по умолчанию отображаются в диалоговом окне Sign. Значение по умолчанию для этого свойства**true**.

**Возвращает:**
boolean — значение, указывающее, что в диалоговом окне «Подпись» отображаются инструкции по умолчанию.
### getEmail() {#getEmail--}
```
public String getEmail()
```


 Получает предполагаемый адрес электронной почты подписывающей стороны. Значение по умолчанию для этого свойства**empty string**.

**Возвращает:**
java.lang.String — Предлагаемый адрес электронной почты подписывающей стороны.
### getInstructions() {#getInstructions--}
```
public String getInstructions()
```


 Получает инструкции для подписывающей стороны, которые отображаются при подписании строки подписи. Значение по умолчанию для этого свойства**empty string**.

**Возвращает:**
java.lang.String — Инструкции для подписавшего, которые отображаются при подписании строки подписи.
### getShowDate() {#getShowDate--}
```
public boolean getShowDate()
```


 Получает значение, указывающее, что дата подписи отображается в строке подписи. Значение по умолчанию для этого свойства**true**.

**Возвращает:**
boolean — значение, указывающее, что дата подписи отображается в строке подписи.
### getSigner() {#getSigner--}
```
public String getSigner()
```


 Получает предполагаемого подписывающего в строке подписи. Значение по умолчанию для этого свойства**empty string**.

**Возвращает:**
java.lang.String — предполагаемый подписывающий в строке подписи.
### getSignerTitle() {#getSignerTitle--}
```
public String getSignerTitle()
```


 Получает предложенный титул подписывающей стороны. Значение по умолчанию для этого свойства**empty string**.

**Возвращает:**
java.lang.String — предлагаемая должность подписывающей стороны.
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




### setAllowComments(boolean value) {#setAllowComments-boolean-}
```
public void setAllowComments(boolean value)
```


 Задает значение, указывающее, что подписывающая сторона может добавлять комментарии в диалоговом окне «Подписать». Значение по умолчанию для этого свойства**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, что подписывающая сторона может добавлять комментарии в диалоговом окне «Подписать». |

### setDefaultInstructions(boolean value) {#setDefaultInstructions-boolean-}
```
public void setDefaultInstructions(boolean value)
```


 Задает значение, указывающее, что в диалоговом окне «Подпись» отображаются инструкции по умолчанию. Значение по умолчанию для этого свойства**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, что инструкции по умолчанию отображаются в диалоговом окне «Подписать». |

### setEmail(String value) {#setEmail-java.lang.String-}
```
public void setEmail(String value)
```


 Устанавливает предполагаемый адрес электронной почты подписывающей стороны. Значение по умолчанию для этого свойства**empty string**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Предлагаемый адрес электронной почты подписывающей стороны. |

### setInstructions(String value) {#setInstructions-java.lang.String-}
```
public void setInstructions(String value)
```


 Задает инструкции для подписывающей стороны, которые отображаются при подписании строки подписи. Значение по умолчанию для этого свойства**empty string**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Инструкции для подписывающего, которые отображаются при подписании строки подписи. |

### setShowDate(boolean value) {#setShowDate-boolean-}
```
public void setShowDate(boolean value)
```


 Задает значение, указывающее, что дата подписи отображается в строке подписи. Значение по умолчанию для этого свойства**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, что дата подписания отображается в строке подписи. |

### setSigner(String value) {#setSigner-java.lang.String-}
```
public void setSigner(String value)
```


 Устанавливает предполагаемого подписывающего в строке подписи. Значение по умолчанию для этого свойства**empty string**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Предлагаемый подписывающий в строке подписи. |

### setSignerTitle(String value) {#setSignerTitle-java.lang.String-}
```
public void setSignerTitle(String value)
```


 Устанавливает предполагаемый титул подписавшего. Значение по умолчанию для этого свойства**empty string**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Предлагаемая должность подписывающего лица. |

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
