---
title: OleFormat
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет доступ к данным объекта OLE или элемента управления ActiveX.
type: docs
weight: 425
url: /ru/java/com.aspose.words/oleformat/
---

**Наследование:**
java.lang.Object
```
public class OleFormat
```

Предоставляет доступ к данным объекта OLE или элемента управления ActiveX.

 Чтобы узнать больше, посетите**Working with Ole Objects** документальная статья.

 Использовать[Shape.getOleFormat()](../../com.aspose.words/shape\#getOleFormat--) свойство для доступа к данным объекта OLE. Вы не создаете экземпляры[OleFormat](../../com.aspose.words/oleformat) класс напрямую.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAutoUpdate()](#getAutoUpdate--) | Указывает, будет ли автоматически обновляться ссылка на объект OLE в Microsoft Word. |
| [getClass()](#getClass--) |  |
| [getClsid()](#getClsid--) | Получает CLSID объекта OLE. |
| [getIconCaption()](#getIconCaption--) | Получает заголовок значка объекта OLE. |
| [getOleControl()](#getOleControl--) |  Получает[getOleControl()](../../com.aspose.words/oleformat\#getOleControl--) объекты, если этот объект OLE является элементом управления ActiveX. |
| [getOleEntry(String oleEntryName)](#getOleEntry-java.lang.String-) |  |
| [getOleIcon()](#getOleIcon--) | Получает аспект отрисовки объекта OLE. |
| [getOlePackage()](#getOlePackage--) |  Предоставить доступ к[OlePackage](../../com.aspose.words/olepackage)если объект OLE является пакетом OLE. |
| [getProgId()](#getProgId--) | Получает ProgID объекта OLE. |
| [getRawData()](#getRawData--) | Получает необработанные данные объекта OLE. |
| [getSourceFullName()](#getSourceFullName--) | Получает путь и имя исходного файла для связанного объекта OLE. |
| [getSourceItem()](#getSourceItem--) | Получает строку, которая используется для идентификации части исходного файла, на которую делается ссылка. |
| [getSuggestedExtension()](#getSuggestedExtension--) | Получает расширение файла, предлагаемое для текущего встроенного объекта, если вы хотите сохранить его в файл. |
| [getSuggestedFileName()](#getSuggestedFileName--) | Получает имя файла, предложенное для текущего встроенного объекта, если вы хотите сохранить его в файл. |
| [hashCode()](#hashCode--) |  |
| [isLink()](#isLink--) |  Возвращает true, если объект OLE связан (когда[getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-)уточняется). |
| [isLocked()](#isLocked--) | Указывает, заблокирована ли ссылка на объект OLE от обновлений. |
| [isLocked(boolean value)](#isLocked-boolean-) | Указывает, заблокирована ли ссылка на объект OLE от обновлений. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [save(OutputStream stream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | Сохраняет данные встроенного объекта в файл с указанным именем. |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean-) | Указывает, будет ли автоматически обновляться ссылка на объект OLE в Microsoft Word. |
| [setProgId(String value)](#setProgId-java.lang.String-) | Задает ProgID объекта OLE. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String-) | Задает путь и имя исходного файла для связанного объекта OLE. |
| [setSourceItem(String value)](#setSourceItem-java.lang.String-) | Задает строку, которая используется для идентификации части исходного файла, на которую делается ссылка. |
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
### getAutoUpdate() {#getAutoUpdate--}
```
public boolean getAutoUpdate()
```


Указывает, будет ли автоматически обновляться ссылка на объект OLE в Microsoft Word.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getClsid() {#getClsid--}
```
public UUID getClsid()
```


Получает CLSID объекта OLE.

**Возвращает:**
java.util.UUID — CLSID объекта OLE.
### getIconCaption() {#getIconCaption--}
```
public String getIconCaption()
```


Получает заголовок значка объекта OLE.

Если объект OLE не встроен, так как невозможно получить значок или заголовок, возвращается пустая строка.

**Возвращает:**
java.lang.String — заголовок значка объекта OLE.
### getOleControl() {#getOleControl--}
```
public OleControl getOleControl()
```


 Получает[getOleControl()](../../com.aspose.words/oleformat\#getOleControl--) объекты, если этот объект OLE является элементом управления ActiveX. В противном случае это свойство равно null.

**Возвращает:**
[OleControl](../../com.aspose.words/olecontrol) -\{[getOleControl()](../../com.aspose.words/oleformat\#getOleControl--) объекты, если этот объект OLE является элементом управления ActiveX.
### getOleEntry(String oleEntryName) {#getOleEntry-java.lang.String-}
```
public byte[] getOleEntry(String oleEntryName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| oleEntryName | java.lang.String |  |

**Возвращает:**
байт[]
### getOleIcon() {#getOleIcon--}
```
public boolean getOleIcon()
```


 Получает аспект отрисовки объекта OLE. Когда**true** , объект OLE отображается в виде значка. Когда**false**, объект OLE отображается как содержимое.

Aspose.Words не позволяет устанавливать это свойство, чтобы избежать путаницы. Если бы вы могли изменить аспект рисования в Aspose.Words, Microsoft Word по-прежнему отображал бы объект OLE в его исходном аспекте рисования, пока вы не отредактируете или не обновите объект OLE в Microsoft Word.

**Возвращает:**
boolean — аспект рисования объекта OLE.
### getOlePackage() {#getOlePackage--}
```
public OlePackage getOlePackage()
```


 Предоставить доступ к[OlePackage](../../com.aspose.words/olepackage) если объект OLE является пакетом OLE. В противном случае возвращает null. Пакет OLE — это устаревшая технология, которая позволяет обернуть любой формат файла, отсутствующий в реестре OLE системы Windows, в общий пакет, позволяющий встраивать в документ практически все, что угодно. Видеть[OlePackage](../../com.aspose.words/olepackage) введите для получения дополнительной информации.

**Возвращает:**
[OlePackage](../../com.aspose.words/olepackage) - соответствующий[OlePackage](../../com.aspose.words/olepackage) ценность.
### getProgId() {#getProgId--}
```
public String getProgId()
```


Получает ProgID объекта OLE.

Свойство ProgID не всегда присутствует в документах Microsoft Word, и на него нельзя полагаться.

Не может быть нулевым.

Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — ProgID объекта OLE.
### getRawData() {#getRawData--}
```
public byte[] getRawData()
```


Получает необработанные данные объекта OLE.

**Возвращает:**
байт[]
### getSourceFullName() {#getSourceFullName--}
```
public String getSourceFullName()
```


Получает путь и имя исходного файла для связанного объекта OLE.

Значение по умолчанию — пустая строка.

 Если[getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-) не является пустой строкой, объект OLE связан.

**Возвращает:**
java.lang.String — путь и имя исходного файла для связанного объекта OLE.
### getSourceItem() {#getSourceItem--}
```
public String getSourceItem()
```


Получает строку, которая используется для идентификации части исходного файла, на которую делается ссылка.

Значение по умолчанию — пустая строка.

 Например, если исходный файл представляет собой книгу Microsoft Excel,[getSourceItem()](../../com.aspose.words/oleformat\#getSourceItem--) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat\#setSourceItem-java.lang.String-) Свойство может возвращать «Workbook1! R3C1: R4C2», если объект OLE содержит только несколько ячеек листа.

**Возвращает:**
java.lang.String — строка, используемая для идентификации части исходного файла, на которую делается ссылка.
### getSuggestedExtension() {#getSuggestedExtension--}
```
public String getSuggestedExtension()
```


Получает расширение файла, предлагаемое для текущего встроенного объекта, если вы хотите сохранить его в файл.

**Возвращает:**
java.lang.String — расширение файла, предлагаемое для текущего встроенного объекта, если вы хотите сохранить его в файл.
### getSuggestedFileName() {#getSuggestedFileName--}
```
public String getSuggestedFileName()
```


Получает имя файла, предложенное для текущего встроенного объекта, если вы хотите сохранить его в файл.

**Возвращает:**
java.lang.String — имя файла, предлагаемое для текущего встроенного объекта, если вы хотите сохранить его в файл.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isLink() {#isLink--}
```
public boolean isLink()
```


 Возвращает true, если объект OLE связан (когда[getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-)уточняется).

**Возвращает:**
 boolean — Истинно, если объект OLE связан (когда[getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-)уточняется).
### isLocked() {#isLocked--}
```
public boolean isLocked()
```


Указывает, заблокирована ли ссылка на объект OLE от обновлений.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


Указывает, заблокирована ли ссылка на объект OLE от обновлений.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### save(OutputStream stream) {#save-java.io.OutputStream-}
```
public void save(OutputStream stream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String-}
```
public void save(String fileName)
```


Сохраняет данные встроенного объекта в файл с указанным именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла для сохранения данных объекта OLE. |

### setAutoUpdate(boolean value) {#setAutoUpdate-boolean-}
```
public void setAutoUpdate(boolean value)
```


Указывает, будет ли автоматически обновляться ссылка на объект OLE в Microsoft Word.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setProgId(String value) {#setProgId-java.lang.String-}
```
public void setProgId(String value)
```


Задает ProgID объекта OLE.

Свойство ProgID не всегда присутствует в документах Microsoft Word, и на него нельзя полагаться.

Не может быть нулевым.

Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | ProgID объекта OLE. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String-}
```
public void setSourceFullName(String value)
```


Задает путь и имя исходного файла для связанного объекта OLE.

Значение по умолчанию — пустая строка.

 Если[getSourceFullName()](../../com.aspose.words/oleformat\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat\#setSourceFullName-java.lang.String-) не является пустой строкой, объект OLE связан.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Путь и имя исходного файла для связанного объекта OLE. |

### setSourceItem(String value) {#setSourceItem-java.lang.String-}
```
public void setSourceItem(String value)
```


Задает строку, которая используется для идентификации части исходного файла, на которую делается ссылка.

Значение по умолчанию — пустая строка.

 Например, если исходный файл представляет собой книгу Microsoft Excel,[getSourceItem()](../../com.aspose.words/oleformat\#getSourceItem--) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat\#setSourceItem-java.lang.String-) Свойство может возвращать «Workbook1! R3C1: R4C2», если объект OLE содержит только несколько ячеек листа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Строка, используемая для идентификации части исходного файла, на которую делается ссылка. |

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
