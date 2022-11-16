---
title: IHyphenationCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуется классами, которые могут регистрировать словари переносов.
type: docs
weight: 647
url: /ru/java/com.aspose.words/ihyphenationcallback/
---
```
public interface IHyphenationCallback
```

Реализуется классами, которые могут регистрировать словари переносов.
## Методы

| Метод | Описание |
| --- | --- |
| [requestDictionary(String language)](#requestDictionary-java.lang.String-) | Уведомляет приложение о том, что словарь переносов для указанного языка не найден и, возможно, его необходимо зарегистрировать. |
### requestDictionary(String language) {#requestDictionary-java.lang.String-}
```
public abstract void requestDictionary(String language)
```


Уведомляет приложение о том, что словарь переносов для указанного языка не найден и, возможно, его необходимо зарегистрировать.

 Реализация должна найти словарь и зарегистрировать его, используя**M:Aspose.Words.Hyphenation.RegisterDictionary(System.String,System.IO.Stream)** методы.

 Если словарь недоступен для указанного языка, реализация может отказаться от дальнейших вызовов для того же языка, используя[Hyphenation.registerDictionary(java.lang.String, java.lang.String)](../../com.aspose.words/hyphenation\#registerDictionary-java.lang.String--java.lang.String-) с нулевым значением.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| language | java.lang.String | Название языка, например "en-US". См. документацию .NET для «имени культуры» и RFC 4646 для получения подробной информации. Исключения, создаваемые этим методом, прервут выполнение процесса макета страницы. |
