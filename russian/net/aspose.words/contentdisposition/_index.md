---
title: ContentDisposition Enum
linktitle: ContentDisposition
articleTitle: ContentDisposition
second_title: Aspose.Words для .NET
description: Изучите перечисление Aspose.Words.ContentDisposition, чтобы открыть для себя различные варианты представления документов для улучшения взаимодействия с клиентским браузером.
type: docs
weight: 540
url: /ru/net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

Перечисляет различные способы представления документа в клиентском браузере.

```csharp
public enum ContentDisposition
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Attachment | `0` | Отправить документ в браузер и предоставить возможность сохранить документ на диск или открыть в приложении , связанном с расширением документа. |
| Inline | `1` | Отправляет документ в браузер и предоставляет возможность сохранить документ на диск или открыть в браузере. |

## Примечания

Обратите внимание, что фактическое поведение клиентского браузера может зависеть от настроек безопасности браузера.

## Примеры

Показывает, как выполнить слияние почты, а затем сохранить документ в клиентском браузере.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Отправляем документ в клиентский браузер.
//Выброшено, потому что HttpResponse имеет значение null в тесте.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Нам нужно будет закрыть этот ответ вручную, чтобы гарантировать, что мы не добавим в документ лишнего содержимого после сохранения.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
