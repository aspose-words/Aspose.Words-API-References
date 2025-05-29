---
title: LoadOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words для .NET
description: Оптимизируйте чтение документов с помощью свойства LoadOptions TempFolder. Легко управляйте временными файлами для эффективной обработки и повышения производительности.
type: docs
weight: 150
url: /ru/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство`нулевой` и временные файлы не используются.

```csharp
public string TempFolder { get; set; }
```

## Примечания

Папка должна существовать и быть доступна для записи, в противном случае будет выдано исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения чтения.

## Примеры

Показывает, как загрузить документ с использованием временных файлов.

```csharp
// Обратите внимание, что такой подход может сократить использование памяти, но снижает скорость
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Убедитесь, что каталог существует, и загрузите
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Показывает, как использовать жесткий диск вместо памяти при загрузке документа.

```csharp
// Когда мы загружаем документ, различные элементы временно сохраняются в памяти, пока происходит операция сохранения.
// Мы можем использовать эту опцию, чтобы использовать временную папку в локальной файловой системе,
// что уменьшит нагрузку на память нашего приложения.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Указанная временная папка должна существовать в локальной файловой системе перед операцией загрузки.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// Папка сохранится без остаточного содержимого после операции загрузки.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
