---
title: DocSaveOptions.SaveRoutingSlip
linktitle: SaveRoutingSlip
articleTitle: SaveRoutingSlip
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DocSaveOptions SaveRoutingSlip. Управляйте сохранением данных RoutingSlip для ваших документов. Легко улучшайте настройку вывода!
type: docs
weight: 70
url: /ru/net/aspose.words.saving/docsaveoptions/saveroutingslip/
---
## DocSaveOptions.SaveRoutingSlip property

Когда`ЛОЖЬ` , Данные RoutingSlip не сохраняются в выходном документе. Значение по умолчанию:`истинный` .

```csharp
public bool SaveRoutingSlip { get; set; }
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

* class [DocSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
