---
title: OoxmlSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SaveFormat в OoxmlSaveOptions, чтобы легко выбирать форматы документов, такие как Docx, Docm, Dotx, Dotm или FlatOpc, для удобного сохранения.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/ooxmlsaveoptions/saveformat/
---
## OoxmlSaveOptions.SaveFormat property

Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может бытьDocx ,Docm , Dotx ,Dotm илиFlatOpc .

```csharp
public override SaveFormat SaveFormat { get; set; }
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
