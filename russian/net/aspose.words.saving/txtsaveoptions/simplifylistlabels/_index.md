---
title: TxtSaveOptions.SimplifyListLabels
linktitle: SimplifyListLabels
articleTitle: SimplifyListLabels
second_title: Aspose.Words для .NET
description: Узнайте, как функция SimplifyListLabels в TxtSaveOptions повышает ясность, упрощая сложные списки и улучшая представление текста.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Указывает, должна ли программа упрощать метки списков в случае, если сложное форматирование меток x000d_ не может быть адекватно представлено простым текстом.

Если установлено значение`истинный` , нумерованные списки записываются в простом числовом формате , а подробные списки — в виде простых символов ASCII. Значение по умолчанию:`ЛОЖЬ`.

```csharp
public bool SimplifyListLabels { get; set; }
```

## Примеры

Показывает, как изменить внешний вид списков при сохранении документа в виде обычного текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать маркированный список с пятью уровнями отступа.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent();
builder.Writeln("Item 3");
builder.ListFormat.ListIndent();
builder.Writeln("Item 4");
builder.ListFormat.ListIndent();
builder.Write("Item 5");

// Создаем объект "TxtSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ сохранения документа в виде обычного текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Установите свойство "SimplifyListLabels" в значение "true", чтобы преобразовать некоторый список
// символы в более простые символы ASCII, такие как '*', 'o', '+', '>' и т. д.
// Установите свойство «SimplifyListLabels» в значение «false», чтобы сохранить как можно больше исходных символов списка.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

string newLine = Environment.NewLine;

if (simplifyListLabels)
    Assert.AreEqual($"* Item 1{newLine}" +
                    $"  > Item 2{newLine}" +
                    $"    + Item 3{newLine}" +
                    $"      - Item 4{newLine}" +
                    $"        o Item 5{newLine}", docText);
else
    Assert.AreEqual($"· Item 1{newLine}" +
                    $"o Item 2{newLine}" +
                    $"§ Item 3{newLine}" +
                    $"· Item 4{newLine}" +
                    $"o Item 5{newLine}", docText);
```

### Смотрите также

* class [TxtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
