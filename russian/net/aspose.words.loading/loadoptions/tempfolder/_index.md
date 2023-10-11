---
title: LoadOptions.TempFolder
second_title: Справочник по API Aspose.Words для .NET
description: LoadOptions свойство. Позволяет использовать временные файлы при чтении документа. По умолчанию это свойствонулевой и никакие временные файлы не используются.
type: docs
weight: 150
url: /ru/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство`нулевой` и никакие временные файлы не используются.

```csharp
public string TempFolder { get; set; }
```

### Примечания

Папка должна существовать и быть доступна для записи, в противном случае будет выдано исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения чтения.

### Примеры

Показывает, как загрузить документ, используя временные файлы.

```csharp
// Обратите внимание, что такой подход может уменьшить использование памяти, но снижает скорость
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Убедитесь, что каталог существует, и загрузите
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Показывает, как использовать жесткий диск вместо памяти при загрузке документа.

```csharp
// Когда мы загружаем документ, различные элементы временно сохраняются в памяти, пока происходит операция сохранения.
// Мы можем использовать эту опцию, чтобы вместо этого использовать временную папку в локальной файловой системе,
// что уменьшит нагрузку на память нашего приложения.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Указанная временная папка должна существовать в локальной файловой системе до операции загрузки.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// Папка сохранится без остаточного содержимого после операции загрузки.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../loadoptions/)
* сборка [Aspose.Words](../../../)


