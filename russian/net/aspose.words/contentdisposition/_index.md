---
title: ContentDisposition Enum
linktitle: ContentDisposition
articleTitle: ContentDisposition
second_title: Aspose.Words для .NET
description: Aspose.Words.ContentDisposition перечисление. Перечисляет различные способы представления документа в клиентском браузере на С#.
type: docs
weight: 340
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
| Attachment | `0` | Отправьте документ в браузер и предоставьте возможность сохранить документ на диск или открыть в приложении , связанном с расширением документа. |
| Inline | `1` | Отправляет документ в браузер и предоставляет возможность сохранить документ на диск или открыть в браузере. |

## Примечания

Обратите внимание, что на фактическое поведение клиентского браузера может влиять конфигурация безопасности браузера.

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
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Выбрасывается, потому что HttpResponse в тесте имеет значение null.

// Нам нужно будет закрыть этот ответ вручную, чтобы гарантировать, что мы не добавим в документ лишний контент после сохранения.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
