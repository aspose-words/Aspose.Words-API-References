---
title: IWarningCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если вы хотите, чтобы ваш собственный метод вызывался для сбора предупреждений о потере точности, которые могут возникнуть во время загрузки или сохранения документа.
type: docs
weight: 661
url: /ru/java/com.aspose.words/iwarningcallback/
---
```
public interface IWarningCallback
```

Реализуйте этот интерфейс, если вы хотите, чтобы ваш собственный метод вызывался для сбора предупреждений о потере точности, которые могут возникнуть во время загрузки или сохранения документа.
## Методы

| Метод | Описание |
| --- | --- |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo-) | Aspose.Words вызывает этот метод, когда во время загрузки или сохранения документа возникает проблема, которая может привести к потере форматирования или точности данных. |
### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo-}
```
public abstract void warning(WarningInfo info)
```


Aspose.Words вызывает этот метод, когда во время загрузки или сохранения документа возникает проблема, которая может привести к потере форматирования или точности данных.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo) |  |
