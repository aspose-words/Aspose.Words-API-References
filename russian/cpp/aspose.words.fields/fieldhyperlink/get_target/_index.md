---
title: "Aspose::Words::Fields::FieldHyperlink::get_Target метод"
linktitle: "get_Target"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldHyperlink::get_Target метод. Получает или задает цель, на которую должна перенаправляться ссылка в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.fields/fieldhyperlink/get_target/
---
## FieldHyperlink::get_Target method


Получает или задает цель, на которую должна перенаправляться ссылка.

```cpp
System::String Aspose::Words::Fields::FieldHyperlink::get_Target()
```


## Примеры



Показывает, как использовать поля HYPERLINK для ссылки на документы в локальной файловой системе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// Когда мы щёлкаем это поле HYPERLINK в Microsoft Word,
// оно откроет связанный документ, а затем разместит курсор в указанной закладке.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// Когда мы щёлкаем это поле HYPERLINK в Microsoft Word,
// оно откроет связанный документ и автоматически прокрутит вниз до указанного iframe.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## См. также

* Class [FieldHyperlink](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
