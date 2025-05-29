---
title: IncorrectPasswordException Class
linktitle: IncorrectPasswordException
articleTitle: IncorrectPasswordException
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.IncorrectPasswordException, который обрабатывает ошибки паролей для зашифрованных документов, обеспечивая безопасный и бесперебойный доступ.
type: docs
weight: 3700
url: /ru/net/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException class

Вызывается, если документ зашифрован паролем, а пароль, указанный при открытии документа, неверен или отсутствует.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) документальная статья.

```csharp
public class IncorrectPasswordException : Exception
```

## Примеры

Показывает, как настроить параметры сохранения для старых форматов Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Установите пароль, который защитит загрузку документа Microsoft Word или Aspose.Words.
// Обратите внимание, что это никак не шифрует содержимое документа.
options.Password = "MyPassword";

// Если документ содержит маршрутный лист, мы можем сохранить его при сохранении, установив этот флаг в значение true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Чтобы иметь возможность загрузить документ,
// нам нужно будет применить пароль, указанный нами в объекте DocSaveOptions, в объекте LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
