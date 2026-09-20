---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars метод"
linktitle: "get_KeepLegacyControlChars"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars метод. Сохраняет оригинальное представление устаревших управляющих символов в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/ooxmlsaveoptions/get_keeplegacycontrolchars/
---
## OoxmlSaveOptions::get_KeepLegacyControlChars method


Сохраняет оригинальное представление устаревших управляющих символов.

```cpp
bool Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars() const
```


## Примеры



Показывает, как поддерживать устаревшие управляющие символы при конвертации в .docx.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// Когда мы сохраняем документ в формат OOXML, мы можем создать объект OoxmlSaveOptions
// а затем передать его методу сохранения документа, чтобы изменить способ сохранения документа.
// Установите свойство \"KeepLegacyControlChars\" в \"true\", чтобы сохранить
// устаревший символ \"ShortDateTime\" при сохранении.
// Установите свойство \"KeepLegacyControlChars\" в \"false\", чтобы удалить
// устаревший символ \"ShortDateTime\" из выходного документа.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## См. также

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
