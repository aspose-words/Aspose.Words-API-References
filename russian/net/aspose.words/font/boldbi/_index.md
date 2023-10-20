---
title: Font.BoldBi
linktitle: BoldBi
articleTitle: BoldBi
second_title: Aspose.Words для .NET
description: Font BoldBi свойство. True если текст написанный справа налево выделен жирным шрифтом на С#.
type: docs
weight: 50
url: /ru/net/aspose.words/font/boldbi/
---
## Font.BoldBi property

True, если текст, написанный справа налево, выделен жирным шрифтом.

```csharp
public bool BoldBi { get; set; }
```

## Примеры

Показывает, как определить отдельные наборы настроек шрифта для текста, написанного справа налево и справа налево.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Определить набор настроек шрифта для текста, написанного слева направо.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Определим другой набор настроек шрифта для текста, написанного справа налево.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Мы можем использовать флаг Bidi, чтобы указать, будет ли текст, который мы собираемся добавить,
// в построителе документов — справа налево. Когда мы добавляем текст с этим флагом, установленным в true,
// он будет отформатирован с использованием набора настроек шрифта с письмом справа налево.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Установите флаг в значение false, а затем добавьте текст слева направо.
// Конструктор документов отформатирует их, используя набор настроек шрифта слева направо.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
