---
title: FieldPrint.PrinterInstructions
linktitle: PrinterInstructions
articleTitle: PrinterInstructions
second_title: Aspose.Words для .NET
description: Узнайте, как управлять управляющими кодами принтера и инструкциями PostScript с помощью FieldPrint PrinterInstructions для оптимизированных решений печати.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldprint/printerinstructions/
---
## FieldPrint.PrinterInstructions property

Возвращает или задает символы управляющего кода принтера или инструкции PostScript.

```csharp
public string PrinterInstructions { get; set; }
```

## Примеры

Показывает, как вставить поле ПЕЧАТЬ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// Поле PRINT может отправлять инструкции на принтер.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Задайте область, в которой принтер будет выполнять инструкции.
// В этом случае это будет абзац, содержащий наше поле PRINT.
field.PostScriptGroup = "para";

// Когда мы используем принтер, поддерживающий PostScript, для печати нашего документа,
// эта команда сделает всю область, указанную нами в "field.PostScriptGroup", белой.
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Смотрите также

* class [FieldPrint](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
