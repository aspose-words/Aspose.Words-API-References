---
title: ImportFormatOptions.ForceCopyStyles
second_title: Справочник по API Aspose.Words для .NET
description: ImportFormatOptions свойство. Получает или задает логическое значение указывающее следует ли копировать конфликтующие стили вKeepSourceFormatting mode. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 30
url: /ru/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Получает или задает логическое значение, указывающее, следует ли копировать конфликтующие стили вKeepSourceFormatting mode. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ForceCopyStyles { get; set; }
```

### Примечания

По умолчанию, если соответствующий стиль уже существует в целевом документе, исходный стиль formatting расширяется до прямых атрибутов узла, а стиль этого узла сбрасывается до значения по умолчанию.

Если для этой опции установлено значение`истинный`, исходный стиль будет принудительно скопирован в целевой документ с уникальным именем и применен к импортированному узлу.

Обратите внимание: в этом случае не гарантируется сохранение форматирования импортированного узла в целевом документе document .

### Примеры

Показывает, как принудительно копировать исходные стили с уникальными именами.

```csharp
// Оба документа содержат MyStyle1 и MyStyle2, MyStyle3 существует только в исходном документе.
Document srcDoc = new Document(MyDir + "Styles source.docx");
Document dstDoc = new Document(MyDir + "Styles destination.docx");

ImportFormatOptions options = new ImportFormatOptions { ForceCopyStyles = true };
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

ParagraphCollection paras = dstDoc.Sections[1].Body.Paragraphs;

Assert.AreEqual(paras[0].ParagraphFormat.Style.Name, "MyStyle1_0");
Assert.AreEqual(paras[1].ParagraphFormat.Style.Name, "MyStyle2_0");
Assert.AreEqual(paras[2].ParagraphFormat.Style.Name, "MyStyle3");
```

### Смотрите также

* class [ImportFormatOptions](../)
* пространство имен [Aspose.Words](../../importformatoptions/)
* сборка [Aspose.Words](../../../)


