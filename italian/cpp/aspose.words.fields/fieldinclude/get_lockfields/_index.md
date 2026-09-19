---
title: "Metodo Aspose::Words::Fields::FieldInclude::get_LockFields"
linktitle: "get_LockFields"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldInclude::get_LockFields. Ottiene o imposta se impedire l'aggiornamento dei campi nel documento incluso in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fields/fieldinclude/get_lockfields/
---
## FieldInclude::get_LockFields method


Ottiene o imposta se impedire l'aggiornamento dei campi nel documento incluso.

```cpp
bool Aspose::Words::Fields::FieldInclude::get_LockFields() override
```


## Esempi



Mostra come creare un campo INCLUDE e impostare le sue proprietà.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Possiamo usare un campo INCLUDE per importare una parte di un altro documento nel file system locale.
// Il segnalibro dell'altro documento a cui facciamo riferimento con questo campo contiene questa parte importata.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```

## Vedi anche

* Class [FieldInclude](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
