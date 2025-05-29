---
title: ShapeMarkupLanguage Enum
linktitle: ShapeMarkupLanguage
articleTitle: ShapeMarkupLanguage
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.ShapeMarkupLanguage, определяющее языки разметки фигур для улучшенного форматирования документов и гибкости дизайна.
type: docs
weight: 1670
url: /ru/net/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enumeration

Указывает язык разметки, используемый для фигуры.

```csharp
public enum ShapeMarkupLanguage : byte
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Dml | `0` | Для определения формы используется язык разметки чертежей. |
| Vml | `1` | Для определения формы используется векторный язык разметки. |

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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
