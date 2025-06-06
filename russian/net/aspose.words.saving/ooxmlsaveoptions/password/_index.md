---
title: OoxmlSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words для .NET
description: Защитите свои документы с помощью OoxmlSaveOptions! Легко установите пароль для шифрования с использованием стандарта ECMA376 для улучшенной защиты данных.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

Получает/устанавливает пароль для шифрования документа с использованием стандартного алгоритма шифрования ECMA376.

```csharp
public string Password { get; set; }
```

## Примечания

Для сохранения документа без шифрования это свойство должно быть`нулевой` или пустая строка.

## Примеры

Показывает, как создать зашифрованный паролем документ Office Open XML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// Мы не сможем открыть этот документ в Microsoft Word или
// Aspose.Words без указания правильного пароля.
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// Откройте зашифрованный документ, передав правильный пароль в объекте LoadOptions.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Смотрите также

* class [OoxmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
