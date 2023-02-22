---
title: TxtSaveOptions.SimplifyListLabels
second_title: Справочник по API Aspose.Words для .NET
description: TxtSaveOptions свойство. Указывает должна ли программа упрощать метки списков в случае если форматирование сложных меток не может быть адекватно представлено простым текстом.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Указывает, должна ли программа упрощать метки списков в случае, если форматирование сложных меток не может быть адекватно представлено простым текстом.

Если установлено **истинный** , метки нумерованных списков записываются в простом числовом формате , а метки детализированных списков — в виде простых символов ASCII. Значение по умолчанию **ЛОЖЬ**.

```csharp
public bool SimplifyListLabels { get; set; }
```

### Примеры

Показывает, как изменить внешний вид списков при сохранении документа в обычный текст.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем маркированный список с пятью уровнями отступов.
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

// Создаем объект "TxtSaveOptions", который мы можем передать в метод "Сохранить" документа
// чтобы изменить способ сохранения документа в виде открытого текста.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Установите для свойства "SimplifyListLabels" значение "true", чтобы преобразовать какой-либо список
// символы в более простые символы ASCII, такие как '*', 'o', '+', '>' и т. д.
// Установите для свойства SimplifyListLabels значение false, чтобы сохранить как можно больше исходных символов списка.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

if (simplifyListLabels)
    Assert.AreEqual("* Item 1\r\n" +
                    "  > Item 2\r\n" +
                    "    + Item 3\r\n" +
                    "      - Item 4\r\n" +
                    "        o Item 5\r\n", docText);
else
    Assert.AreEqual("· Item 1\r\n" +
                    "o Item 2\r\n" +
                    "§ Item 3\r\n" +
                    "· Item 4\r\n" +
                    "o Item 5\r\n", docText);
```

### Смотрите также

* class [TxtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../txtsaveoptions/)
* сборка [Aspose.Words](../../../)


