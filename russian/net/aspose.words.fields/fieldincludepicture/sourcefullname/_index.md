---
title: FieldIncludePicture.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldIncludePicture SourceFullName. Легко управляйте местоположениями изображений с помощью IRI для улучшенной интеграции мультимедиа и бесперебойного пользовательского опыта.
type: docs
weight: 60
url: /ru/net/aspose.words.fields/fieldincludepicture/sourcefullname/
---
## FieldIncludePicture.SourceFullName property

Получает или задает местоположение изображения с помощью IRI.

```csharp
public string SourceFullName { get; set; }
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

* class [FieldIncludePicture](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
