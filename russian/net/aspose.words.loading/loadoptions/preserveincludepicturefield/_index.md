---
title: LoadOptions.PreserveIncludePictureField
linktitle: PreserveIncludePictureField
articleTitle: PreserveIncludePictureField
second_title: Aspose.Words для .NET
description: Управляйте полем INCLUDEPICTURE в форматах Microsoft Word с помощью LoadOptions PreserveIncludePictureField. Легко управляйте форматированием документа для достижения оптимальных результатов.
type: docs
weight: 120
url: /ru/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Возвращает или задает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool PreserveIncludePictureField { get; set; }
```

## Примечания

По умолчанию поле INCLUDEPICTURE преобразуется в объект формы. Вы можете переопределить это, если вам нужно сохранить поле, например, если вы хотите обновить его программно. Однако обратите внимание, что этот подход не является общепринятым для Aspose.Words. Используйте его на свой страх и риск.

Одним из возможных вариантов использования может быть использование MERGEFIELD в качестве дочернего поля для динамического изменения исходного path изображения. В этом случае вам необходимо сохранить INCLUDEPICTURE в модели.

## Примеры

Показывает, как сохранить или удалить поля INCLUDEPICTURE при загрузке документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Мы можем установить флаг в объекте LoadOptions, чтобы решить, следует ли преобразовывать все поля INCLUDEPICTURE
    // в фигуры изображений при загрузке документа, который их содержит.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
