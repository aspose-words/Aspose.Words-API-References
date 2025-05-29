---
title: FieldImport.IsLinked
linktitle: IsLinked
articleTitle: IsLinked
second_title: Aspose.Words для .NET
description: Оптимизируйте свои документы с помощью свойства IsLinked в FieldImport, чтобы уменьшить размер файла, исключив графические данные. Повысьте эффективность и производительность сегодня!
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldimport/islinked/
---
## FieldImport.IsLinked property

Возвращает или задает, следует ли уменьшить размер файла, не сохраняя графические данные вместе с документом.

```csharp
public bool IsLinked { get; set; }
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
