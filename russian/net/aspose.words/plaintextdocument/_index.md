---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.PlainTextDocument, который позволит вам легко извлекать и использовать открытый текст из ваших документов для улучшения их читаемости и обработки.
type: docs
weight: 5170
url: /ru/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Позволяет извлечь текстовое представление содержимого документа.

Чтобы узнать больше, посетите[Работа с текстовым документом](https://docs.aspose.com/words/net/working-with-text-document/) документальная статья.

```csharp
public class PlainTextDocument
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(*Stream*) | Создает простой текстовый документ из потока. Автоматически определяет формат файла. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(*string*) | Создает простой текстовый документ из файла. Автоматически определяет формат файла. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Создает простой текстовый документ из потока. Позволяет указать дополнительные параметры, такие как пароль шифрования. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Создает простой текстовый документ из файла. Позволяет указать дополнительные параметры, такие как пароль шифрования. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | Получает[`BuiltInDocumentProperties`](./builtindocumentproperties/) документа. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | Получает[`CustomDocumentProperties`](./customdocumentproperties/) документа. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Получает текстовое содержимое документа, объединенное в строку. |

## Примеры

Показывает, как загрузить содержимое документа Microsoft Word в виде обычного текста.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
