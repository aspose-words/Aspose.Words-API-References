---
title: OoxmlSaveOptions.SaveFormat
second_title: Справочник по API Aspose.Words для .NET
description: OoxmlSaveOptions свойство. Указывает формат в котором документ будет сохранен если используется этот объект параметров сохранения. Может бытьDocx Docm  Dotx Dotm илиFlatOpc .
type: docs
weight: 60
url: /ru/net/aspose.words.saving/ooxmlsaveoptions/saveformat/
---
## OoxmlSaveOptions.SaveFormat property

Указывает формат, в котором документ будет сохранен, если используется этот объект параметров сохранения. Может бытьDocx ,Docm , Dotx ,Dotm илиFlatOpc .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Примеры

Показывает, как установить спецификацию соответствия OOXML для сохраненного документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы настроим параметры совместимости для соответствия Microsoft Word 2003,
// вставка изображения определит его форму с помощью VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// Стандарт OOXML «ISO/IEC 29500:2008» не поддерживает формы VML.
// Если мы установим для свойства «Соответствие» объекта SaveOptions значение «OoxmlCompliance.Iso29500_2008_Strict»,
 // любой документ, который мы сохраняем при передаче этого объекта, должен будет соответствовать этому стандарту.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Наш сохраненный документ определяет форму с использованием DML, чтобы соответствовать стандарту OOXML «ISO/IEC 29500:2008».
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* сборка [Aspose.Words](../../../)


