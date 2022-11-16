---
title: IDocumentReaderPlugin
second_title: Справочник по API Aspose.Words для Java
description: Определяет интерфейс для внешних подключаемых модулей чтения, которые могут считывать файл в документ.
type: docs
weight: 638
url: /ru/java/com.aspose.words/idocumentreaderplugin/
---
```
public interface IDocumentReaderPlugin
```

Определяет интерфейс для внешних подключаемых модулей чтения, которые могут считывать файл в документ.
## Методы

| Метод | Описание |
| --- | --- |
| [read(InputStream src, LoadOptions loadOptions, Document document)](#read-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.Document-) |  |
### read(InputStream src, LoadOptions loadOptions, Document document) {#read-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.Document-}
```
public abstract void read(InputStream src, LoadOptions loadOptions, Document document)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| src | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) |  |
| document | [Document](../../com.aspose.words/document) |  |
