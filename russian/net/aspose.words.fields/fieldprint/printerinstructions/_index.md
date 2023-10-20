---
title: FieldPrint.PrinterInstructions
linktitle: PrinterInstructions
articleTitle: PrinterInstructions
second_title: Aspose.Words для .NET
description: FieldPrint PrinterInstructions свойство. Получает или задает символы управляющего кода принтера или инструкции PostScript на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldprint/printerinstructions/
---
## FieldPrint.PrinterInstructions property

Получает или задает символы управляющего кода принтера или инструкции PostScript.

```csharp
public string PrinterInstructions { get; set; }
```

## Примеры

Показывает, что нужно вставить поле ПЕЧАТЬ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// Поле ПЕЧАТЬ может отправлять инструкции на принтер.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Установите область, в которой принтер будет выполнять инструкции.
// В данном случае это будет абзац, содержащий наше поле PRINT.
field.PostScriptGroup = "para";

// Когда мы используем принтер, поддерживающий PostScript, для печати нашего документа,
// эта команда превратит всю область, указанную в «field.PostScriptGroup», в белую.
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Смотрите также

* class [FieldPrint](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
