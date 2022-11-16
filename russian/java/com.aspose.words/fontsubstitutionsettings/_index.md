---
title: FontSubstitutionSettings
second_title: Справочник по API Aspose.Words для Java
description: Задает настройки механизма подстановки шрифтов.
type: docs
weight: 290
url: /ru/java/com.aspose.words/fontsubstitutionsettings/
---

**Наследование:**
java.lang.Object
```
public class FontSubstitutionSettings
```

Задает настройки механизма подстановки шрифтов.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.

Процесс замены шрифта состоит из нескольких правил, которые проверяются одно за другим в определенном порядке. Если первое правило не может разрешить шрифт, проверяется второе правило и так далее.

Порядок правил следующий: 1. Правило подстановки имени шрифта (по умолчанию включено) 2. Правило подстановки конфигурации шрифта (по умолчанию отключено) 3. Правило подстановки таблицы (по умолчанию включено) 4. Правило подстановки информации о шрифте (по умолчанию включено) ) 5. Правило шрифта по умолчанию (по умолчанию включено)

 Обратите внимание, что правило подстановки информации о шрифте всегда разрешает шрифт, если[FontInfo](../../com.aspose.words/fontinfo) доступен и переопределит правило шрифта по умолчанию. Если вы хотите использовать правило шрифта по умолчанию, вам следует отключить правило подстановки информации о шрифте.

Обратите внимание, что правило подстановки конфигурации шрифта разрешает шрифт в большинстве случаев и, таким образом, переопределяет все другие правила.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDefaultFontSubstitution()](#getDefaultFontSubstitution--) | Настройки, связанные с правилом замены шрифта по умолчанию. |
| [getFontConfigSubstitution()](#getFontConfigSubstitution--) | Настройки, связанные с правилом подстановки конфигурации шрифта. |
| [getFontInfoSubstitution()](#getFontInfoSubstitution--) | Настройки, связанные с правилом подстановки информации о шрифте. |
| [getFontNameSubstitution()](#getFontNameSubstitution--) | Настройки, связанные с правилом подстановки имени шрифта. |
| [getTableSubstitution()](#getTableSubstitution--) | Настройки, связанные с правилом подстановки таблиц. |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDefaultFontSubstitution() {#getDefaultFontSubstitution--}
```
public DefaultFontSubstitutionRule getDefaultFontSubstitution()
```


Настройки, связанные с правилом замены шрифта по умолчанию.

**Возвращает:**
[DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule) - соответствующий[DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule) ценность.
### getFontConfigSubstitution() {#getFontConfigSubstitution--}
```
public FontConfigSubstitutionRule getFontConfigSubstitution()
```


Настройки, связанные с правилом подстановки конфигурации шрифта.

**Возвращает:**
[FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule) - соответствующий[FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule) ценность.
### getFontInfoSubstitution() {#getFontInfoSubstitution--}
```
public FontInfoSubstitutionRule getFontInfoSubstitution()
```


Настройки, связанные с правилом подстановки информации о шрифте.

**Возвращает:**
[FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule) - соответствующий[FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule) ценность.
### getFontNameSubstitution() {#getFontNameSubstitution--}
```
public FontNameSubstitutionRule getFontNameSubstitution()
```


Настройки, связанные с правилом подстановки имени шрифта.

**Возвращает:**
[FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule) - соответствующий[FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule) ценность.
### getTableSubstitution() {#getTableSubstitution--}
```
public TableSubstitutionRule getTableSubstitution()
```


Настройки, связанные с правилом подстановки таблиц.

**Возвращает:**
[TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule) - соответствующий[TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule) ценность.
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
