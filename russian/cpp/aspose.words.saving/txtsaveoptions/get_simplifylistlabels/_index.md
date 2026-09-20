---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels method"
linktitle: "get_SimplifyListLabels"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels метод. Указывает, следует ли программе упрощать метки списков в случае, когда сложное форматирование меток недостаточно представимо в простом тексте. Если установить значение true, метки нумерованных списков записываются в простом числовом формате, а метки маркированных списков — в виде простых ASCII‑символов. Значение по умолчанию — false в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.saving/txtsaveoptions/get_simplifylistlabels/
---
## TxtSaveOptions::get_SimplifyListLabels method


Указывает, должна ли программа упрощать метки списков в случае, когда сложное форматирование меток не может быть адекватно представлено в простом тексте. Если установить **true**, метки нумерованных списков будут записываться в простом числовом формате, а маркеры маркированных списков — в виде простых ASCII‑символов. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels() const
```


## Примеры



Показывает, как изменить внешний вид списков при сохранении документа в простой текст.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте маркированный список с пятью уровнями отступов.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 3");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 4");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 5");

// Создайте объект "TxtSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ сохранения документа в простой текст.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Установите свойство "SimplifyListLabels" в "true", чтобы преобразовать некоторые списки
// символы в более простые ASCII‑символы, такие как '*', 'o', '+', '>', и т.д.
// Установите свойство "SimplifyListLabels" в "false", чтобы сохранить как можно больше оригинальных символов списка.
txtSaveOptions->set_SimplifyListLabels(simplifyListLabels);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt");

System::String newLine = System::Environment::get_NewLine();
if (simplifyListLabels)
{
    ASSERT_EQ(System::String::Format(u"* Item 1{0}", newLine) + System::String::Format(u"  > Item 2{0}", newLine) + System::String::Format(u"    + Item 3{0}", newLine) + System::String::Format(u"      - Item 4{0}", newLine) + System::String::Format(u"        o Item 5{0}", newLine), docText);
}
else
{
    ASSERT_EQ(System::String::Format(u"· Item 1{0}", newLine) + System::String::Format(u"o Item 2{0}", newLine) + System::String::Format(u"§ Item 3{0}", newLine) + System::String::Format(u"· Item 4{0}", newLine) + System::String::Format(u"o Item 5{0}", newLine), docText);
}
```

## См. также

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
