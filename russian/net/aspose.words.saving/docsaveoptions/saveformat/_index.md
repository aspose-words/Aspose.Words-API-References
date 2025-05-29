---
title: DocSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DocSaveOptions SaveFormat, чтобы легко выбирать между форматами Doc или Dot для бесперебойного сохранения документов. Оптимизируйте свой рабочий процесс сегодня!
type: docs
weight: 50
url: /ru/net/aspose.words.saving/docsaveoptions/saveformat/
---
## DocSaveOptions.SaveFormat property

Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может бытьDoc илиDot .

```csharp
public override SaveFormat SaveFormat { get; set; }
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [DocSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
