---
title: LoadOptions.MswVersion
linktitle: MswVersion
articleTitle: MswVersion
second_title: Aspose.Words для .NET
description: Оптимизируйте загрузку документов с помощью LoadOptions MswVersion. Обеспечьте совместимость с определенными версиями MS Word, используя по умолчанию Word 2019 для бесшовной интеграции.
type: docs
weight: 100
url: /ru/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

Позволяет указать, что процесс загрузки документа должен соответствовать определенной версии MS Word. Значение по умолчанию:Word2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

## Примечания

Различные версии Word могут обрабатывать некоторые аспекты содержимого документа и форматирования немного по-разному во время процесса загрузки, что может привести к незначительным различиям в объектной модели документа.

## Примеры

Показывает, как эмулировать процедуру загрузки определенной версии Microsoft Word во время загрузки документа.

```csharp
// По умолчанию Aspose.Words загружает документы в соответствии со спецификацией Microsoft Word 2019.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// В этом документе отсутствует стиль форматирования абзацев по умолчанию.
// Этот стиль по умолчанию будет восстановлен при загрузке документа с помощью Microsoft Word или Aspose.Words.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// Межстрочный интервал стиля будет иметь это значение при загрузке спецификацией Microsoft Word 2007.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### Смотрите также

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
