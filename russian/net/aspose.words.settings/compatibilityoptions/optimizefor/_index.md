---
title: OptimizeFor
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет оптимизировать содержимое документа а также поведение Aspose.Words по умолчанию для определенных версий MS Word.
type: docs
weight: 720
url: /ru/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

Позволяет оптимизировать содержимое документа, а также поведение Aspose.Words по умолчанию для определенных версий MS Word.

Используйте этот метод, чтобы MS Word не отображал ленту «Режим совместимости» при загрузке документа. (Обратите внимание, что вам также может потребоваться установить[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance/) собственность на Iso29500_2008_Transitional или выше.)

```csharp
public void OptimizeFor(MsWordVersion version)
```

### Примеры

Показывает, как вертикально выровнять текстовое содержимое текстового поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Установите для свойства "VerticalAnchor" значение "TextBoxAnchor.Top", чтобы
// выровняйте текст в этом текстовом поле по верхней стороне фигуры.
// Установите для свойства "VerticalAnchor" значение "TextBoxAnchor.Middle", чтобы
// выравниваем текст в этом текстовом поле по центру фигуры.
// Установите для свойства "VerticalAnchor" значение "TextBoxAnchor.Bottom", чтобы
// выравниваем текст в этом текстовом поле по нижней части фигуры.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Вертикальное выравнивание текста внутри текстовых полей доступно, начиная с Microsoft Word 2007.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

Показывает, как установить спецификацию соответствия OOXML для сохраненного документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы настроим параметры совместимости для соответствия Microsoft Word 2003,
// вставка изображения определит его форму с помощью VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// Стандарт OOXML "ISO/IEC 29500:2008" не поддерживает формы VML.
// Если мы установим для свойства "Соответствие" объекта SaveOptions значение "OoxmlCompliance.Iso29500_2008_Strict",
 // любой документ, который мы сохраняем при передаче этого объекта, должен соответствовать этому стандарту.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Наш сохраненный документ определяет форму с помощью DML, чтобы соответствовать стандарту OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

Показывает, как оптимизировать документ для разных версий Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Этот объект содержит обширный список флагов, уникальных для каждого документа
    // которые позволяют нам обеспечить обратную совместимость со старыми версиями Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Печать настроек по умолчанию для пустого документа.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Мы можем получить доступ к этим настройкам в Microsoft Word через «Файл» -> "Опции" -> «Дополнительно» -> "Параметры совместимости для...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Мы можем использовать метод OptimizeFor, чтобы обеспечить оптимальную совместимость с определенной версией Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Группирует все флаги в объекте параметров совместимости документа по состоянию, а затем печатает каждую группу.
/// </summary>
private static void PrintCompatibilityOptions(CompatibilityOptions options)
{
    for (int i = 1; i >= 0; i--)
    {
        Console.WriteLine(Convert.ToBoolean(i) ? "\tEnabled options:" : "\tDisabled options:");
        SortedSet<string> optionNames = new SortedSet<string>();

        foreach (System.ComponentModel.PropertyDescriptor descriptor in System.ComponentModel.TypeDescriptor.GetProperties(options))
        {
            if (descriptor.PropertyType == Type.GetType("System.Boolean") && i == Convert.ToInt32(descriptor.GetValue(options)))
            {
                optionNames.Add(descriptor.Name);
            }
        }

        foreach (string s in optionNames)
        {
            Console.WriteLine($"\t\t{s}");
        }
    }
}
```

### Смотрите также

* enum [MsWordVersion](../../mswordversion/)
* class [CompatibilityOptions](../)
* пространство имен [Aspose.Words.Settings](../../compatibilityoptions/)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
