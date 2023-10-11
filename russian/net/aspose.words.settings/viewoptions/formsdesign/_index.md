---
title: ViewOptions.FormsDesign
second_title: Справочник по API Aspose.Words для .NET
description: ViewOptions свойство. Указывает находится ли документ в режиме разработки форм.
type: docs
weight: 30
url: /ru/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

Указывает, находится ли документ в режиме разработки форм.

```csharp
public bool FormsDesign { get; set; }
```

### Примечания

На данный момент работает только для документов в формате WordML.

### Примеры

Показывает, как включить/отключить режим разработки форм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Установите для свойства «FormsDesign» значение «false», чтобы режим дизайна форм был отключен.
// Установите для свойства FormsDesign значение true, чтобы включить режим разработки форм.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### Смотрите также

* class [ViewOptions](../)
* пространство имен [Aspose.Words.Settings](../../viewoptions/)
* сборка [Aspose.Words](../../../)


