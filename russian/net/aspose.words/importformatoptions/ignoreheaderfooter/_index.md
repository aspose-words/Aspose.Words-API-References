---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImportFormatOptions IgnoreHeaderFooter, управляйте форматированием верхнего/нижнего колонтитула в режиме KeepSourceFormatting. Упростите импорт документов сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Возвращает или задает логическое значение, указывающее, что исходное форматирование содержимого верхних/нижних колонтитулов игнорируется , еслиKeepSourceFormatting используется режим . Значение по умолчанию:`истинный` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Примеры

Показывает, как указать, следует ли игнорировать исходное форматирование содержимого верхних/нижних колонтитулов.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

// Если 'IgnoreHeaderFooter' имеет значение false, то исходное форматирование содержимого верхнего/нижнего колонтитула
// будет использовано из "Типы верхних и нижних колонтитулов.docx".
// Если 'IgnoreHeaderFooter' имеет значение true, то форматирование содержимого верхнего/нижнего колонтитула
// из "Document.docx" будет использован.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Смотрите также

* class [ImportFormatOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
