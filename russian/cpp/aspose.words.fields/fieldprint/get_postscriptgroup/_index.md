---
title: "Метод Aspose::Words::Fields::FieldPrint::get_PostScriptGroup"
linktitle: "get_PostScriptGroup"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::FieldPrint::get_PostScriptGroup. Получает или задает прямоугольник рисования, на котором работают инструкции PostScript, в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fieldprint/get_postscriptgroup/
---
## FieldPrint::get_PostScriptGroup method


Получает или задает прямоугольник рисования, на котором работают инструкции PostScript.

```cpp
System::String Aspose::Words::Fields::FieldPrint::get_PostScriptGroup()
```


## Примеры



Показывает, как вставить поле PRINT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"My paragraph");

// Поле PRINT может отправлять инструкции принтеру.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrint>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPrint, true));

// Установите область, над которой принтер будет выполнять инструкции.
// В этом случае это будет абзац, содержащий наше поле PRINT.
field->set_PostScriptGroup(u"para");

// Когда мы используем принтер, поддерживающий PostScript, для печати нашего документа,
// эта команда сделает полностью белой всю область, которую мы указали в "field.PostScriptGroup".
field->set_PrinterInstructions(u"erasepage");

ASSERT_EQ(u" PRINT  erasepage \\p para", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.PRINT.docx");
```

## См. также

* Class [FieldPrint](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
