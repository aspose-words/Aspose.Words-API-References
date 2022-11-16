---
title: IFieldUpdateCultureProvider
second_title: Справочник по API Aspose.Words для Java
description: При реализации предоставляет объект, который следует использовать при обновлении определенного поля.
type: docs
weight: 643
url: /ru/java/com.aspose.words/ifieldupdatecultureprovider/
---
```
public interface IFieldUpdateCultureProvider
```

 При реализации обеспечивает[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) объект, который следует использовать при обновлении конкретного поля.
## Методы

| Метод | Описание |
| --- | --- |
| [getCulture(String culture, Field field)](#getCulture-java.lang.String-com.aspose.words.Field-) |  Возвращает[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) объект, который будет использоваться во время обновления поля. |
### getCulture(String culture, Field field) {#getCulture-java.lang.String-com.aspose.words.Field-}
```
public abstract System.Globalization.CultureInfo getCulture(String culture, Field field)
```


 Возвращает[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) объект, который будет использоваться во время обновления поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| culture | java.lang.String | Имя языка и региональных параметров, запрошенное для обновляемого поля. |
| field | [Field](../../com.aspose.words/field) | Поле обновляется. |

**Возвращает:**
[CultureInfo](../../com.aspose.words.net.system.globalization/cultureinfo) - Объект культуры, который следует использовать для обновления поля.