---
title: OoxmlSaveOptions
linktitle: OoxmlSaveOptions
articleTitle: OoxmlSaveOptions
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор OoxmlSaveOptions для легкого сохранения документов в формате Docx. Откройте для себя бесперебойное управление документами и улучшенную совместимость.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions() {#constructor}

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вDocx формат.

```csharp
public OoxmlSaveOptions()
```

## Примеры

Показывает, как задать спецификацию соответствия OOXML для сохраненного документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы настроим параметры совместимости для соответствия Microsoft Word 2003,
// вставка изображения определит его форму с помощью VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// Стандарт OOXML "ISO/IEC 29500:2008" не поддерживает формы VML.
// Если мы установим свойство «Compliance» объекта SaveOptions на «OoxmlCompliance.Iso29500_2008_Strict»,
 // любой документ, который мы сохраняем при передаче этого объекта, должен будет соответствовать этому стандарту.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Наш сохраненный документ определяет форму с помощью DML для соответствия стандарту OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Смотрите также

* class [OoxmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)

---

## OoxmlSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа вDocx , Docm ,Dotx ,Dotm или FlatOpc формат.

```csharp
public OoxmlSaveOptions(SaveFormat saveFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | SaveFormat | Может бытьDocx ,Docm , Dotx ,Dotm илиFlatOpc . |

## Примеры

Показывает, как обеспечить поддержку устаревших управляющих символов при конвертации в .docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Когда мы сохраняем документ в формате OOXML, мы можем создать объект OoxmlSaveOptions
// а затем передаем его в метод сохранения документа, чтобы изменить способ сохранения документа.
// Установите свойство "KeepLegacyControlChars" в значение "true", чтобы сохранить
// устаревший символ "ShortDateTime" при сохранении.
// Установите свойство "KeepLegacyControlChars" в значение "false", чтобы удалить
// устаревший символ "ShortDateTime" из выходного документа.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
