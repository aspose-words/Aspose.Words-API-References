---
title: FieldIncludePicture.ResizeHorizontally
second_title: Справочник по API Aspose.Words для .NET
description: FieldIncludePicture свойство. Получает или задает следует ли изменять размер изображения по горизонтали из источника.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldincludepicture/resizehorizontally/
---
## FieldIncludePicture.ResizeHorizontally property

Получает или задает, следует ли изменять размер изображения по горизонтали из источника.

```csharp
public bool ResizeHorizontally { get; set; }
```

### Примеры

Показывает, как вставлять изображения с помощью полей IMPORT и INCLUDEPICTURE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два похожих типа полей, которые мы можем использовать для отображения изображений, связанных из локальной файловой системы.
// 1 - Поле INCLUDEPICTURE:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Применяем фильтр PNG32.FLT.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - Поле ИМПОРТ:
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### Смотрите также

* class [FieldIncludePicture](../)
* пространство имен [Aspose.Words.Fields](../../fieldincludepicture/)
* сборка [Aspose.Words](../../../)


