---
title: FieldImport.GraphicFilter
linktitle: GraphicFilter
articleTitle: GraphicFilter
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldImport GraphicFilter, позволяющее легко устанавливать или извлекать фильтры графического формата, улучшая процесс вставки контента.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldimport/graphicfilter/
---
## FieldImport.GraphicFilter property

Возвращает или задает имя фильтра для формата вставляемого графического объекта.

```csharp
public string GraphicFilter { get; set; }
```

## Примеры

Показывает, как вставлять изображения с помощью полей IMPORT и INCLUDEPICTURE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два похожих типа полей, которые мы можем использовать для отображения изображений, связанных с локальной файловой системой.
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

* class [FieldImport](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
